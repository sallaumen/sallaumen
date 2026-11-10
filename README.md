# Lucas Tavano

Backend engineer in Curitiba, Brazil. I've written Elixir since 2019, most of it in fintech. These days I work at XSeed and spend the rest of my time on tooling for coding agents: how they get their instructions, how I watch them work, and where a human has to say yes.

## What I'm building

### [Elixir Agent Kit](https://github.com/sallaumen/elixir-agent-kit)

Coding-agent practices shipped as a Mix dependency. A project pins a tag, and every agent that works on it (Codex, Claude Code, your own harness) reads the same reviewed workflows from `deps/`: what to inspect, which decisions matter, what counts as proof that the work is done.

The alternative is a folder of skill files copied into each repository, which stop agreeing with each other within weeks. Here a workflow improves once, ships as a tag, and each project adopts it in an ordinary dependency PR. `mix agent_kit.check` runs offline in CI and fails when the references drift. There is no service and no model call, and nothing ships to production.

### [DSH Super Agent Board](https://github.com/sallaumen/dsh-superagent-superboard)

A Phoenix LiveView board for work that starts on GitHub. An external agent (DeepSeek Super Agent) executes the tickets. The board shows issues, pull requests, reviews, checks and agent tickets across repositories as they change, dispatches Claude Code or Codex on my machine with spending limits, and asks for confirmation before anything consequential.

I use it to run my own projects, with more than one agent writing to the same repository. Most of what I've learned about agents came from the failures it made visible.

### Smaller things

- [LocalWebMonitorex](https://github.com/sallaumen/LocalWebMonitorex): a local LiveView dashboard that watches the web apps running on localhost.
- [deckex](https://github.com/sallaumen/deckex): Commander deck analysis. It measures the deck, asks an LLM for changes, then checks every suggestion against real card data (color identity, legality, price) before showing it. README in Portuguese.
- [camerex](https://github.com/sallaumen/camerex): turns dance photos and videos into neon rotoscopy, fully local, with U²-Net, OpenCV and Nx. README in Portuguese.

## Where I'm going with this

I want one person to be able to run several agents across several projects and still know what each one did and why. In my experience that depends less on the model than on ordinary engineering: versioned instructions, visible state, a spending limit, a human gate before anything irreversible. OTP was built for supervising many unreliable processes, which is why all of this is in Elixir.

## Background

Eight years as a backend engineer. I started with PHP and embedded Linux and moved to Elixir in 2019.

- **Vic.ai**: AP automation, invoice processing, payment orchestration, accounting integrations.
- **SWAP**: payment authorizations and real-time data processing, as Elixir Specialist and technical lead.
- **EBANX**: monitoring for financial systems and large data pipelines.

In 2022 I co-presented "Comparing Elixir and Python for Simple Neural Networks" at CodeBEAM America, benchmarking Nx against Keras. The [paper](https://github.com/sallaumen/elixir_vs_python_nn_performance_comparison) and the [Elixir code](https://github.com/sallaumen/elixir_neural_network_labs) are public.

## Contact

[LinkedIn](https://www.linkedin.com/in/lucas-c-tavano-1b0092169/) · [lucas.c.tavano@gmail.com](mailto:lucas.c.tavano@gmail.com)

I'm open to conversations about Elixir backend work and agent tooling.
