# Globalping: Native API Reference

A consolidated summary of Globalping's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://globalping.io/docs/api.globalping.io
- **OpenAPI specification:** https://api.globalping.io/v1/spec.yaml
- **API base URL:** `https://api.globalping.io`

## Authentication

### Access Token

Use a Globalping access token from the Globalping Dashboard to get higher rate limits and credit-backed measurements.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://globalping.io/docs/api.globalping.io)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud Globalping App` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create DNS A Measurement](actions/create-dns-a-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS AAAA Measurement](actions/create-dns-aaaa-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS CNAME Measurement](actions/create-dns-cname-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS HTTPS Measurement](actions/create-dns-https-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS MX Measurement](actions/create-dns-mx-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS NS Measurement](actions/create-dns-ns-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS PTR Measurement](actions/create-dns-ptr-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS SOA Measurement](actions/create-dns-soa-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS SRV Measurement](actions/create-dns-srv-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS Trace Measurement](actions/create-dns-trace-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create DNS TXT Measurement](actions/create-dns-txt-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create HTTP GET Measurement](actions/create-http-get-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create HTTP HEAD Measurement](actions/create-http-head-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create HTTP OPTIONS Measurement](actions/create-http-options-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create HTTP2 GET Measurement](actions/create-http2-get-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create IPv6 HTTP GET Measurement](actions/create-ipv6-http-get-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create IPv6 Ping Measurement](actions/create-ipv6-ping-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create IPv6 Traceroute Measurement](actions/create-ipv6-traceroute-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create Live Ping Measurement](actions/create-live-ping-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create MTR Measurement](actions/create-mtr-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create Ping Measurement](actions/create-ping-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create TCP MTR Measurement](actions/create-tcp-mtr-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create TCP Ping Measurement](actions/create-tcp-ping-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create TCP Traceroute Measurement](actions/create-tcp-traceroute-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create Traceroute Measurement](actions/create-traceroute-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create UDP MTR Measurement](actions/create-udp-mtr-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Create UDP Traceroute Measurement](actions/create-udp-traceroute-measurement.md) | `POST /v1/measurements` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Get Limits](actions/get-limits.md) | `GET /v1/limits` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [Get Measurement](actions/get-measurement.md) | `GET /v1/measurements/:id` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
| [List Probes](actions/list-probes.md) | `GET /v1/probes` | [docs](https://github.com/jsdelivr/globalping#globalping-rest-api) |
