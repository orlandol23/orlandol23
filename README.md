# Orlando Fernandes

**Senior Software Engineer** · React / TypeScript · Java · AI-augmented development
Natal, Brazil (UTC-3) · Remote · [LinkedIn](https://linkedin.com/in/orlando-fernandes-de-lima-e-silva-a37a69140)

5+ years building web applications, mostly React and TypeScript, with a full-stack foundation in Java/Spring. I care about the parts that don't show up in a screenshot: profiling before optimizing, tests that actually catch things, and READMEs that don't promise more than the code delivers.

I work AI-augmented every day (Claude Code as a primary tool, multi-agent review as a standard quality gate), and I build on-chain on the side.

---

### What I've been working on

**[ai-dlh](https://github.com/orlandol23/ai-dlh)** · On-chain learning hub
React + tRPC + Drizzle/Postgres with a Solidity contract [deployed and source-verified on Sepolia](https://sepolia.etherscan.io/address/0x3C399AdD53c70DC828db096d6b953757494427CE). The interesting part isn't the contract, it's the write pipeline that puts data on it: atomic claim, replace-by-fee, error taxonomy, idempotency by partial unique index. Wallet-signature auth with domain binding and an atomically consumed nonce. End-to-end type safety from the contract to the UI.
`React` `TypeScript` `tRPC` `Drizzle` `Solidity` `viem`

**[ai-boxing-instructor](https://github.com/orlandol23/ai-boxing-instructor)** · Real-time boxing coach in the browser · [live demo](https://ai-boxing-instructor.vercel.app)
Pose detection runs entirely client-side via MediaPipe, so no video ever leaves the device. The boxing logic lives in a pure, React-free engine that's testable with fixtures. AI coaching from the Claude API degrades gracefully: without an API key the coaching panel disappears and everything else keeps working.
`React 19` `TypeScript strict` `MediaPipe` `Claude API` `PWA`

**[swiss-defi-optimizer](https://github.com/orlandol23/swiss-defi-optimizer)** · ERC-4626 vault
A tokenized vault inheriting OpenZeppelin 5.0.2, with reentrancy guards, a deposit cap enforced consistently across `deposit` and `mint`, and Chainlink price conversion. Contracts only, and the README says so.
`Solidity` `Hardhat` `OpenZeppelin` `Chainlink`

---

### Two things I learned the hard way

**A 23-second UI freeze that wasn't where I thought.** A 400-item page locked up on every sort. I built a Playwright/CDP profiling harness before changing a line, and the CPU profile showed ~2,400 tooltip instances accounted for ~93% of the cost. Refactoring to a single global tooltip across 533 call sites took the production sort from 16,830ms to 545ms, validated across three independent measurements.

**A background worker that quietly burned a monthly quota.** My side project's database kept hitting its compute limit with zero traffic. The cause was a queue worker polling Postgres every 15 seconds. On a serverless database that bills for time awake, it simply never hibernated. Backoff when the queue is empty cut the estimated usage by roughly 6x.

---

### Working with

`TypeScript` `JavaScript` `React` `Next.js` `React Native` `Node.js` `Java` `Spring Boot`
`Zustand` `Tailwind` `Radix/shadcn` `Jest` `Vitest` `Testing Library` `Cypress` `Playwright`
`PostgreSQL` `Drizzle` `REST` `tRPC` `Vite` `pnpm` `AWS` `Solidity` `Hardhat` `viem`
`Claude Code` `MCP` `multi-agent review` `LLM APIs`

**Open to remote roles:** senior frontend, full-stack, or AI-native. Based in Brazil, no sponsorship needed, full overlap with the Americas and most of Europe.

📫 orlandu.lima@gmail.com
