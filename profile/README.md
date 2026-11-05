DatRail is an open-source project and organization building tools that learn what your AI agents actually use and do (their resources, data and APIs) and alert you when that behavior drifts from what you approved.

## 🚀 Start here

**[datrail-project](https://github.com/datrail/datrail-project#readme)** runs the open-source DatRail stack on your own machine. Already running an agent in a container? One command installs DatRail and points it at your agent, asking which one:

```bash
curl -fsSL https://raw.githubusercontent.com/datrail/datrail-project/master/install.sh | bash
```

Or clone the repository and start the stack with its demo agent:

```bash
git clone https://github.com/datrail/datrail-project.git
cd datrail-project
docker compose up -d
```

Then open <http://127.0.0.1:8000>. RailMon watches the agent and delivers its evidence to RailDash automatically; you lock a baseline and see drift as it happens. The [install guide](https://github.com/datrail/datrail-project/blob/master/INSTALL.md) has the details, with step-by-step pages for a [Mac](https://github.com/datrail/datrail-project/blob/master/docs/setup-mac.md) and for [Windows](https://github.com/datrail/datrail-project/blob/master/docs/setup-windows.md), and a page an [AI agent can follow](https://github.com/datrail/datrail-project/blob/master/docs/agent-install.md) to do the install for you. The [glossary](https://github.com/datrail/datrail-project/blob/master/docs/glossary.md) explains the terms: evidence bundle, Agent Security Profile (ASP), baseline, alignment, drift.

## 🧩 Components

| Repository | What it does |
| --- | --- |
| [datrail-project](https://github.com/datrail/datrail-project#readme) | The entry point: the one-command install, the Compose stack, install guides and glossary. |
| [RailMon](https://github.com/datrail/railmon#readme) | Collects evidence about a running agent: its TLS traffic, the ports it opens, the files it opens, and periodic scans of its environment, delivered as evidence bundles. |
| [RailDash](https://github.com/datrail/raildash#readme) | Local dashboard. Turns evidence bundles into Agent Security Profiles (ASPs), locks baselines, shows drift and holds the Data Guardrail. |
| [eBPF TLS Tap](https://github.com/datrail/ebpf-tls-tap#readme) | Standalone Linux eBPF probes: `sslsniff` (TLS plaintext), `listensnoop` (listening sockets) and `filesnoop` (file opens). RailMon itself records all of these with AgentSight. |
| [DatRail Proxy](https://github.com/datrail/proxy#readme) | Sits between an agent and its MCP servers and attaches an `x-rail` identity ticket to each call. |
| [DatRail Gateway](https://github.com/datrail/gateway#readme) | Sits in front of an MCP server, checks the `x-rail` ticket against policy, and forwards or refuses the call. |

## 🛡️ Our Mission

As AI agents become a seamless part of daily work, end users—who often lack deep security backgrounds—need a simple way to protect their personal and proprietary data.

DatRail brings enterprise-grade data and infrastructure security best practices into an accessible, open-source tool. By drawing on years of expertise in securing complex systems, we make it effortless for anyone to set up automatic guardrails that safeguard sensitive information whenever an AI agent's behavior strays from what it was approved to do.

## 🤝 Community Driven, Enterprise Sponsored

DatRail operates at the intersection of open-source innovation and enterprise cybersecurity:

* Sponsored by [RailXia](https://railxia.com): As an enterprise cybersecurity startup, RailXia acts as the primary sponsor and commercial steward of the DatRail organization. RailXia invests directly into DatRail's open-source codebase, maintaining its core architecture and ensuring the project remains freely accessible, transparent, and robust for the broader developer community.
* Collaboration with [Eunomia](https://eunomia.dev): Built in deep collaboration with the [Eunomia open-source community](https://eunomia.dev/), DatRail leverages Eunomia’s eBPF tools to enable light-weight introspection/observability for applicable AI workloads.
