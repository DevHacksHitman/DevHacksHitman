# Hi, I'm Dev Kik

Systems and Web3 engineer. I build small, dependency-light software that has
to survive bad conditions: flaky HLS streams, slow disks, peers that lie
about content length, and users who close the laptop mid-download.

Mostly that means JS/TS frontends, Python tooling, Rust services, and Go for
GRAM (TVM) contracts — the chain the world still calls TON — plus EVM and
Solana when the state has to be provable.

## Shipped

**[hundjager](https://github.com/DevHacksHitman/hundjager)** — a local media
extraction hub wrapping yt-dlp. One ~800-line Python file, standard library
only, no pip install, and a UI on top. The part I actually sweated wasn't
the streaming — it was the threat model: a localhost web server any random
webpage can reach is an attack surface, so it has a Host/Origin/Sec-Fetch-Site
filter, DNS-rebinding defense, and a bounded task registry. 32 tests, mocked
subprocesses, no network required to run them.

**art_sol** — an on-chain game on Solana: Anchor programs, PDA-derived
state, time-vault mechanics, optimistic UI hydration. Private while
competitive — ask me about the state derivation, it's the fun part.

**HALO** — an agentic mutual-aid fund experiment. Scoped MetaMask
permissions, agent-to-agent messaging, relayer payouts, wallet-scoped UX.
It taught me that "the contract is safe" and "the people holding the keys
are safe" are different problems.

## Now building

**solana-liquidity-stream-tracker** — async Solana market monitor:
WebSocket liquidity listener, block parser, non-blocking analytics writer.
Private today; goes public after a security pass.

**edge url shortener** — Rust, axum + Tokio. The redirect never waits on
the analytics counter: non-blocking writer, Base62 keys, SQLx. The design
doc survived three rewrites.

## How I work

- Dependency-free bias: if the standard library solves it, there's no package.json
- Money and outside networks mean threat model first
- Tests where failure is silent (parsers, security filters), hand-verification where failure is loud
- I read logs more than I write documentation

Rust's ownership model is making me a better Python programmer, which was
not the plan. On-chain security — Solana and EVM — is the long-term rabbit
hole. Newest experiments: GRAM/TVM contracts and a Telegram mini app,
releasing soon.

Outside the terminal: chess, farming, animals. Biologist by education,
engineer by training.

## Contact

Fastest: issues and PRs on anything above.
Networking and job offers: Telegram — [@kriev_mev](https://t.me/kriev_mev)
