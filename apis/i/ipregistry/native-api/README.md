# Ipregistry: Native API Reference

A consolidated summary of Ipregistry's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://ipregistry.co/docs/
- **API base URL:** `https://api.ipregistry.co`

## Authentication

### API Key

Connect Ipregistry with an API key sent in the Authorization header as `ApiKey YOUR_API_KEY`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ipregistry.co/docs/authentication)

## API conventions

Response data is read from `data`.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get ASN Lookup](actions/get-asn-lookup.md) | `GET /:asn` | [docs](https://ipregistry.co/docs/endpoints#single-as) |
| [Get Batch ASN Lookup](actions/get-batch-asn-lookup.md) | `GET /:asns` | [docs](https://ipregistry.co/docs/endpoints#batch-as) |
| [Get Batch IP Lookup](actions/get-batch-ip-lookup.md) | `GET /:ipAddresses` | [docs](https://ipregistry.co/docs/endpoints#batch-ip) |
| [Get IP Lookup](actions/get-ip-lookup.md) | `GET /:ipAddress` | [docs](https://ipregistry.co/docs/endpoints#single-ip) |
| [Get Origin ASN Lookup](actions/get-origin-asn-lookup.md) | `GET /AS` | [docs](https://ipregistry.co/docs/endpoints#origin-as) |
| [Get Origin IP Lookup](actions/get-origin-ip-lookup.md) | `GET /` | [docs](https://ipregistry.co/docs/endpoints#origin-ip) |
| [Parse Origin User Agent](actions/parse-origin-user-agent.md) | `GET /user_agent` | [docs](https://ipregistry.co/docs/endpoints#origin-user-agent) |
| [Parse User Agents](actions/parse-user-agents.md) | `POST /user_agent` | [docs](https://ipregistry.co/docs/endpoints#batch-user-agent) |
