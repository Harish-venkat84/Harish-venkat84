<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=4000&pause=1000&color=6C63FF&center=true&vCenter=true&multiline=true&repeat=true&width=760&height=160&lines=Hi+%F0%9F%91%8B%2C+I'm+Harish+V;Full+Stack+Engineer;I+build+things+that+move+money+%28safely%29;Open+to+new+roles+%F0%9F%9A%80" alt="Typing SVG" />
</h1>

<p align="center">
  <a href="mailto:harish.venkatesan23@gmail.com"><img src="https://img.shields.io/badge/Open_to_work-2EA44F?style=for-the-badge&logo=handshake&logoColor=white" /></a>
  <a href="https://harish-portfolio-eight-kohl.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-6C63FF?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/harish-software-engineer/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:harish.venkatesan23@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <img src="https://komarev.com/ghpvc/?username=Harish-venkat84&style=for-the-badge&color=6C63FF" alt="Profile Views" />
</p>

---

## `$ whoami`

```yaml
name: Harish V
role: Full Stack Engineer
status: open to new roles 🚀
loves: [real-time systems, backends that handle money, zero-knowledge crypto]
currently_building: [Quietkey, Bahi, XAU Fundamentals, Portfolio, Icon Studio]
fun_fact: "I store money as integer paise. Floats are not invited."
```

- ⚡ Built **production trading systems**: spot + futures matching engines, 15+ NestJS microservices, 10,000+ concurrent WebSocket connections
- 🛠️ Now shipping **my own products end to end**: web, Android and CLI clients, APIs, background workers, CI/CD and self-hosting on a VPS
- 🔐 Comfortable where correctness matters: money ledgers, client-side encryption, idempotent imports, auth done properly
- 🌐 More on my **[portfolio website](https://harish-portfolio-eight-kohl.vercel.app)** (Next.js, Framer Motion, Tailwind CSS)

---

## 🛠️ Side Quests: what I've been building

> Most of these live in private repos (happy to walk through the code in an interview). **Quietkey** is live with open sign-ups, and **Icon Studio** is open source.

<table>
<tr>
<td valign="top" width="50%">

### 🔐 Quietkey
**A zero-knowledge password manager for developers.** The server only ever sees ciphertext.

- Argon2id key derivation + XChaCha20-Poly1305 via libsodium, all on the device
- **Web app, Android app and a CLI** sharing one vault
- Logins, cards and notes, plus **servers, API keys and SSH keys**; `qk run -- <cmd>` and `qk ssh` inject secrets as env vars, so no more `.env` files lying around
- Passkeys or TOTP as a second factor, or a trusted phone's fingerprint
- **Teams:** shared vaults, with keys handed between devices only after comparing fingerprints
- Android: fingerprint unlock, autofill, offline read-only copy, 2FA QR scanning
- Recovery key, and `qk recover` opens a backup offline if the server is ever gone
- 380+ tests, plus Playwright e2e in CI against the production images

<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" /> <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" /> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" /> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" /> <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" /> <img src="https://img.shields.io/badge/libsodium-4B32C3?style=flat-square" /> <img src="https://img.shields.io/badge/Cloudflare_Tunnel-F38020?style=flat-square&logo=cloudflare&logoColor=white" />

<a href="https://quietkey.in"><img src="https://img.shields.io/badge/quietkey.in-2EA44F?style=for-the-badge&logo=googlechrome&logoColor=white" /></a> <a href="https://app.quietkey.in"><img src="https://img.shields.io/badge/Open_the_app-161B22?style=for-the-badge&logo=lock&logoColor=white" /></a>

`🟢 live · 🔒 private repo`

</td>
<td valign="top" width="50%">

### 📒 Bahi <sub>(working name)</sub>
**Personal finance for India, mobile first.** Your bank statements, finally making sense.

- Imports bank statements (CSV/XLS/XLSX), deduplicated: re-uploading inserts nothing new
- Auto-categorization: learned rules → credit card bill detection → income → merchant keywords
- Microservices: HTTP gateway, identity and finance services over NestJS TCP, ingestion worker on BullMQ
- Rotating refresh tokens; a replayed token revokes the whole session family
- Money is always integer paise (`bigint`). Never floats.

<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/BullMQ-CC342D?style=flat-square&logo=redis&logoColor=white" /> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" /> <img src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white" /> <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" />

`🔒 private repo`

</td>
</tr>
<tr>
<td valign="top" width="50%">

### 🥇 XAU Fundamentals
**A gold (XAUUSD) outlook bot that reads the Fed so I don't have to.**

- Pulls Fed speeches and FOMC statements, macro releases, yields, the dollar and central-bank gold flows
- Rule-based **−100 → +100** bias for 2–6 weeks and 3–12 months, with the bull and bear case spelled out
- Claude rates each Fed text **and must quote it word for word**, or the reading is thrown out
- Explains what moved the score since last week, and what each upcoming release would do to it if it comes in hotter, in line or cooler
- Scores its own track record against "always bullish" and "last four weeks" yardsticks
- Tracks my own chart levels and pings me on Telegram
- Decision support only. It never places a trade.

<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black" /> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" /> <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=claude&logoColor=white" /> <img src="https://img.shields.io/badge/Telegram-26A5E4?style=flat-square&logo=telegram&logoColor=white" />

`🔒 private repo`

</td>
<td valign="top" width="50%">

### 📊 Portfolio
**Indian stocks, US stocks and crypto in one ledger.** My first serious Rust project. 🦀

- Binance sync reconciled against live balances; API keys with trading or withdrawal rights are refused
- Zerodha tradebook import with corporate actions, Kite holdings check and Tickertape sync for US stocks
- Daily prices, net worth, FIFO P&L, returns against benchmarks, drawdowns, volatility and correlation
- **Indian tax reports:** capital gains per FY, Schedule FA, Form 67 and tax-loss harvesting, exported for the CA
- Credentials encrypted at rest (XChaCha20-Poly1305), compile-time checked SQL
- CI builds and publishes Docker images on every push to `main`

<img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" /> <img src="https://img.shields.io/badge/axum-6E4A2E?style=flat-square" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />

`🔒 private repo`

</td>
</tr>
<tr>
<td valign="top" colspan="2">

### 🎨 Icon Studio <sub>open source</sub>
**A self-hosted icon studio.** Upload SVGs and PNGs in a web UI, tune them, and ship a typed, tree-shakable **React** and **React Native** package. No database: your icons live in Git, and every save is a commit.

- Uploaded SVGs are sanitized (scripts, event handlers, `foreignObject`, external links stripped) and optimized with SVGO
- Live preview at any size and color; single-color icons follow `currentColor`, multi-color icons expose colors as props
- Generated package: one module per icon, typed props, no hooks and no `'use client'`, so it works in Server Components and React Native
- Releases from the UI: bump the version and CI builds, publishes to npm and tags the commit
- Writes to a local checkout, or commits through the GitHub API when it runs on a server

<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" /> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" /> <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" /> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" /> <img src="https://img.shields.io/badge/SVGO-3E7FC1?style=flat-square&logo=svg&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" /> <img src="https://img.shields.io/badge/npm-CB3837?style=flat-square&logo=npm&logoColor=white" />

<a href="https://github.com/Harish-venkat84/icon-studio"><img src="https://img.shields.io/badge/Source-181717?style=for-the-badge&logo=github&logoColor=white" /></a> <a href="https://icon-studio-three.vercel.app"><img src="https://img.shields.io/badge/Live_demo-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>

`🌐 open source · MIT`

</td>
</tr>
</table>

---

## 💼 Previous Experience: Cryptocurrency Exchange Platform

A production-grade crypto exchange (think Binance) with **3 frontend apps**, **15+ NestJS microservices** and real-time market data infrastructure.

<table>
<tr>
<td valign="top" width="50%">

**Trading Engines**
- FIFO matching engine for fair, deterministic order execution
- Futures engine with isolated/cross margin, leverage and automated liquidation
- Spot engine with limit, market and presale orders
- Take-Profit/Stop-Loss automation, cutting manual intervention by 90%

</td>
<td valign="top" width="50%">

**Real-Time Infrastructure**
- 10 WebSocket gateways handling 10,000+ concurrent connections
- Redis-backed Socket.io adapter for horizontal scaling (99.9% message delivery)
- Live price feeds from Binance, MEXC, Bybit, Kraken, KuCoin and OKX
- Protobuf binary messages, cutting payload size by 60%

</td>
</tr>
<tr>
<td valign="top" width="50%">

**Architecture**
- API gateway with rate limiting and JWT auth
- CQRS + Event Sourcing with EventStore DB and Kafka
- Bull queues for distributed async processing
- OHLC candlestick pipeline feeding TradingView charts

</td>
<td valign="top" width="50%">

**Frontend Applications**
- **Trader Platform**: real-time charts, order books, portfolio
- **Admin Dashboard**: monitoring, users and KYC, fee configuration
- **CRM**: live agent chat, campaigns, support workflows

</td>
</tr>
</table>

---

## 🧰 Tech Stack

<table>
<tr>
<td valign="top" width="33%">

**Frontend & Mobile**

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
</p>

</td>
<td valign="top" width="33%">

**Backend**

<p>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socket.io&logoColor=white" />
  <img src="https://img.shields.io/badge/BullMQ-CC342D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white" />
  <img src="https://img.shields.io/badge/libsodium-4B32C3?style=flat-square" />
  <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=claude&logoColor=white" />
</p>

</td>
<td valign="top" width="33%">

**Data, DevOps & Testing**

<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white" />
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white" />
  <img src="https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white" />
  <img src="https://img.shields.io/badge/pnpm-F69220?style=flat-square&logo=pnpm&logoColor=white" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" />
</p>

</td>
</tr>
</table>

---

## 😄 Lessons Learned the Hard Way

| # | Lesson |
|---|--------|
| 1 | `0.1 + 0.2 !== 0.3`. Never let a float near money. |
| 2 | If the server can read it, it isn't zero-knowledge. |
| 3 | Every queue needs a retry policy, and every retry needs to be idempotent. |
| 4 | "It works on my machine" is not a deployment strategy. Docker is. |

---

## 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Harish-venkat84&theme=tokyonight&hide_border=true" height="170" />
</p>

<p align="center"><sub>Most of my recent work lives in private repos, so the graph undersells it. 🙂</sub></p>

---

## 🐍 Contribution Snake

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Harish-venkat84/Harish-venkat84/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Harish-venkat84/Harish-venkat84/output/github-snake.svg" />
    <img alt="github contribution snake animation" src="https://raw.githubusercontent.com/Harish-venkat84/Harish-venkat84/output/github-snake.svg" />
  </picture>
</p>

---

<p align="center">
  <i>"Building software that handles money and secrets: carefully, and with a sense of humour."</i>
</p>
