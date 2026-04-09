## Notable Projects

### AI Web Agent & WebMCP Benchmark
**Tech Stack:** [Python, Playwright, React, JavaScript, HTML/CSS, Docker Compose]  
An autonomous web agent that navigates and completes tasks across websites using multiple LLMs, with a benchmarking framework evaluating the impact of WebMCP tool exposure on agent performance.

**How it works:** The agent receives a natural language task, observes the current page state through one of two interchangeable modes (screenshot-based visual reasoning or DOM parsing, with or without the additional WebMCP tool invocation), and decides on actions using an LLM. It executes the decided action through Playwright, re-observing the page after each action to decide the next step. A retry and error-recovery layer handles unexpected page states, timeouts, and navigation failures.

**Architecture:** 
- An LLM abstraction layer allowing hot-swapping between models (e.g. GPT-4, Claude, Gemini) with a unified prompt interface
- A React-based dashboard for monitoring agent runs, viewing action logs, and inspecting page observations in real time
- Dockerized benchmark websites with Docker Compose, each configured with and without WebMCP tool declarations for controlled comparison

**Results:**
- ~45% task completion on a WebArena benchmark website via BrowserGym integration
- Designing a 800+ benchmark tasks across 5 Dockerized websites evaluating WebMCP's impact on agent reliability
---

Note: My work is in private repositories
