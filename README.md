# mcp-proxy-agent

A dead-simple, no-bullshit boilerplate to optimize Agentic AI systems (Cline, Roo Code, OpenCode, Windsurf, etc.) for token savings. 

By grouping your tools behind a single proxy and lazy-loading them, you keep your context clean, your response times fast, and your API bills low.

---

## What's Inside

* **configs/agent-config.jsonc**: Your main agent cockpit. Set up your proxy gate and plug in your LSPs.
* **configs/mcp-proxy.jsonc**: The tool shed. Stack whatever heavy MCP servers you want here (Playwright, Git, Memory) without bloating your active session.

---

## Get It Running

### 1. The Strategy
Instead of jamming 20 tools directly into your AI agent on startup, you run them through a proxy. The agent only reads a tiny index. The full heavy specs are loaded on-demand only when the AI actually needs to trigger the tool.

### 2. Setup
1. **Grab a proxy:** Install an MCP multiplexer/compressor (like Atlassian's mcp-compressor).
2. **Configure:** Open configs/agent-config.jsonc and configs/mcp-proxy.jsonc.
3. **Customize:** All hardcoded stacks have been stripped out. Drop your own executable paths, custom LSPs, and preferred MCP args into the blank strings `""`.
4. **Deploy:** Copy them into your AI client's configuration folder.

---

## License
MIT. Do whatever you want with it.
