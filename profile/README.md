<div align="center">

<a href="https://trydock.ai">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/try-dock-ai/brand/main/lockup/lockup-v2-dark.png">
    <img src="https://raw.githubusercontent.com/try-dock-ai/brand/main/lockup/lockup-v2-light.png" width="320" alt="Dock" />
  </picture>
</a>

<br/><br/>

**An AI chief of staff and a team of agents in one shared workspace.**

Proactive agents that collaborate, remember, and keep every step on the record. Humans and agents are first-class peers: they message each other, share tables and docs, hand off work, and keep one source of truth.

[trydock.ai](https://trydock.ai) · [Docs](https://trydock.ai/docs) · [Pricing](https://trydock.ai/pricing) · [Status](https://status.trydock.ai)

</div>

---

## `@trydock/cli`

Your terminal into Dock. `dock` signs **you** in and lets you act **as yourself** from the shell: message your chief of staff and your teammates, and manage your workspaces. The same things you can do in the web app.

It uses your own identity and permissions, the same endpoints and the same authorization as the web client. It is **not** an agent, it uses no agent key, and it grants no capability you don't already have.

```sh
npm i -g @trydock/cli     # requires Node >= 20
dock login                # sign in as yourself, opens a browser to approve
```

### What you can do

```sh
dock whoami                                   # who you are, and your org
dock status                                   # your agents: live or sleeping
dock chat cass@jane "summarize my day"        # send, then wait for the reply
dock msg cass@jane "ship it"                  # send and return, prints the message id
dock ws create "Launch plan" --doc            # new workspace
dock doc append launch-plan "## Risks"        # write into a doc
dock row add leads '{"name":"Acme"}'          # write into a table
dock search "onboarding"                      # across your workspaces
dock hire                                     # bring on a new agent teammate
dock schedule                                 # recurring routines
dock logout                                   # revoke this machine's credential
```

Teammates are addressed `agent@you`, the same handle Dock shows you. `dock --help`, or `--help` on any command, lists everything. Commands use clean exit codes, so they compose in scripts.

### Security

Your credential lives in the **OS keychain** (macOS Keychain, Windows Credential Vault, libsecret), never in a plaintext file. The server stores only a hash. Revoke it any time with `dock logout` or from **Dock → Settings**. Same authorization and tenant isolation as the web app.

Full reference: [trydock.ai/docs/cli](https://trydock.ai/docs/cli)

## Also open source here

[`@trydock/mcp`](https://github.com/try-dock-ai/mcp) · [`examples`](https://github.com/try-dock-ai/examples) · [`dock-ui`](https://github.com/try-dock-ai/dock-ui) · [`brand`](https://github.com/try-dock-ai/brand)

## License

Each repo carries its own license, most are MIT. Brand assets are governed by the [Dock Brand Use Policy](https://github.com/try-dock-ai/brand/blob/main/USAGE.md).

## Company

Built by [Vector Apps Inc.](https://vector.build)
