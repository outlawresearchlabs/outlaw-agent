# outlaw.agent

Autonomous agent identity on the [Handshake](https://handshake.org/) naming protocol, registered via [HeadlessDomains](https://headlessdomains.com) MPP (Machine Payments Protocol) on the [Tempo](https://tempo.xyz) network.

## Identity

| Field | Value |
|-------|-------|
| **Domain** | `outlaw.agent` |
| **Network** | Tempo Mainnet (Chain ID 4217) |
| **Wallet** | `0x9C52373DC45041D9575FbD6ab1c769f6CCc3E8bd` |
| **Registration TX** | `0x23fd61e7dbf839557f43768fb75727f988ff2cb9c1e3589e299c4a20ec9da713` |
| **Payment** | 0.52 PathUSD via MPP |

## What is this?

outlaw.agent is an autonomous agent identity built by [Outlaw Research Labs](https://github.com/nickorlabs). It operates on the Tempo blockchain using the Machine Payments Protocol for agent-to-agent and agent-to-service commerce.

## Stack

- **Identity**: Handshake domain via HeadlessDomains
- **Payments**: Tempo MPP with PathUSD stablecoins
- **Registration**: [headlessdomains-mpp-skill](https://github.com/outlawresearchlabs/headlessdomains-mpp-skill) (corrected v1.2.0)

## API Auth Tiers

| Tier | Token | Access |
|------|-------|--------|
| **Public** | None | health, info, models |
| **Authed** | Any Bearer token | dns, whois, ollama |
| **Admin** | Admin Bearer token | recon, scan, exploit, claude, swarm |

```bash
# Public
curl http://outlaw.run/health

# Authed
curl -H "Authorization: Bearer any-token" http://outlaw.run/task \
  -d '{"type":"dns","target":"example.com"}'

# Admin
curl -H "Authorization: Bearer ADMIN_TOKEN" http://outlaw.run/task \
  -d '{"type":"recon","target":"example.com"}'
```

## License

MIT
