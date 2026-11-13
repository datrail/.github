# Getting help with DatRail

Thanks for trying DatRail. Here is where to go, depending on what you need.

## Start with the docs

Most install problems are already covered:

- [Install guide](https://github.com/datrail/datrail-project/blob/master/INSTALL.md), with step-by-step pages for a [Mac](https://github.com/datrail/datrail-project/blob/master/docs/setup-mac.md) and for [Windows](https://github.com/datrail/datrail-project/blob/master/docs/setup-windows.md)
- [Troubleshooting](https://github.com/datrail/datrail-project/blob/master/INSTALL.md#troubleshooting): no interactions, no ASPs, drift after a restart or an upgrade
- [Platform support](https://github.com/datrail/datrail-project/blob/master/INSTALL.md#platform-support): what DatRail can watch on Linux, Windows (WSL2) and macOS
- [Glossary](https://github.com/datrail/datrail-project/blob/master/docs/glossary.md): evidence bundle, Agent Security Profile (ASP), baseline, alignment, drift

## Ask a question

For "how do I", "is this expected" or "can DatRail do this", ask in [Discussions, Q&A](https://github.com/orgs/datrail/discussions/categories/q-a). Others can find the answer there later.

## Report a bug

If something is broken, open an issue in the repository it belongs to, using the bug report form. If you're not sure which one, use [datrail-project](https://github.com/datrail/datrail-project/issues/new/choose) and we'll move it.

| Repository | Open an issue for |
| --- | --- |
| [datrail-project](https://github.com/datrail/datrail-project/issues/new/choose) | The one-command install, the Compose stack, the install guides |
| [railmon](https://github.com/datrail/railmon/issues/new/choose) | Capture: TLS traffic, ports, files, scans, evidence bundles |
| [raildash](https://github.com/datrail/raildash/issues/new/choose) | The dashboard: ASPs, baselines, drift, the Data Guardrail |
| [ebpf-tls-tap](https://github.com/datrail/ebpf-tls-tap/issues/new/choose) | The standalone eBPF probes |

The form asks for your platform, the versions you run and the logs. With those we can usually answer on the first reply.

## Report a security problem

Please don't open a public issue. Report it privately from the Security tab of the repository it affects: [railmon](https://github.com/datrail/railmon/security/advisories/new), [raildash](https://github.com/datrail/raildash/security/advisories/new) or [ebpf-tls-tap](https://github.com/datrail/ebpf-tls-tap/security/advisories/new). If it's in the install or you're not sure, use railmon's. DatRail sees what agents send and receive, so we treat these reports as urgent.

## Suggest a feature

Open a feature request in the same repositories, or start a thread in [Discussions, Ideas](https://github.com/orgs/datrail/discussions/categories/ideas) if you'd like to talk it through first.

## Email us

For anything that doesn't fit GitHub, or if you'd rather not post in public, email [datrail-support@railxia.com](mailto:datrail-support@railxia.com). Questions and bugs are still best on GitHub, where others can find the answer later. Please report security problems privately on GitHub (above), not by email, and leave tokens, keys and logs out of emails.

## Before you paste logs

Logs and evidence can include what your agent sent and received. Remove tokens, keys, file contents and anything else private before you post them.
