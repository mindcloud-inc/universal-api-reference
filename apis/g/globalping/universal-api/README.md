# <img src="https://images.mindcloud.co/apps/icons/images-18_1774902798572.jpeg" alt="Globalping logo" width="28" height="28"> Globalping: Universal API

Run global network measurements, inspect probe availability, and check account rate limits through the Globalping API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/globalping/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://globalping.io
- **Vendor API docs:** https://globalping.io/docs/api.globalping.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Limits](actions/get-limits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create DNS A Measurement](actions/create-dns-a-measurement.md) | POST | Creates a DNS A measurement in Globalping. |
| [Create DNS AAAA Measurement](actions/create-dns-aaaa-measurement.md) | POST | Creates a DNS AAAA measurement in Globalping. |
| [Create DNS CNAME Measurement](actions/create-dns-cname-measurement.md) | POST | Creates a DNS CNAME measurement in Globalping. |
| [Create DNS HTTPS Measurement](actions/create-dns-https-measurement.md) | POST | Creates a DNS HTTPS measurement in Globalping. |
| [Create DNS MX Measurement](actions/create-dns-mx-measurement.md) | POST | Creates a DNS MX measurement in Globalping. |
| [Create DNS NS Measurement](actions/create-dns-ns-measurement.md) | POST | Creates a DNS NS measurement in Globalping. |
| [Create DNS PTR Measurement](actions/create-dns-ptr-measurement.md) | POST | Creates a DNS PTR measurement in Globalping. |
| [Create DNS SOA Measurement](actions/create-dns-soa-measurement.md) | POST | Creates a DNS SOA measurement in Globalping. |
| [Create DNS SRV Measurement](actions/create-dns-srv-measurement.md) | POST | Creates a DNS SRV measurement in Globalping. |
| [Create DNS Trace Measurement](actions/create-dns-trace-measurement.md) | POST | Creates a DNS trace measurement in Globalping. |
| [Create DNS TXT Measurement](actions/create-dns-txt-measurement.md) | POST | Creates a DNS TXT measurement in Globalping. |
| [Create HTTP GET Measurement](actions/create-http-get-measurement.md) | POST | Creates an HTTP GET measurement in Globalping. |
| [Create HTTP HEAD Measurement](actions/create-http-head-measurement.md) | POST | Creates an HTTP HEAD measurement in Globalping. |
| [Create HTTP OPTIONS Measurement](actions/create-http-options-measurement.md) | POST | Creates an HTTP OPTIONS measurement in Globalping. |
| [Create HTTP2 GET Measurement](actions/create-http2-get-measurement.md) | POST | Creates an HTTP2 GET measurement in Globalping. |
| [Create IPv6 HTTP GET Measurement](actions/create-ipv6-http-get-measurement.md) | POST | Creates an IPv6 HTTP GET measurement in Globalping. |
| [Create IPv6 Ping Measurement](actions/create-ipv6-ping-measurement.md) | POST | Creates an IPv6 ping measurement in Globalping. |
| [Create IPv6 Traceroute Measurement](actions/create-ipv6-traceroute-measurement.md) | POST | Creates an IPv6 traceroute measurement in Globalping. |
| [Create Live Ping Measurement](actions/create-live-ping-measurement.md) | POST | Creates a live ping measurement in Globalping. |
| [Create MTR Measurement](actions/create-mtr-measurement.md) | POST | Creates an MTR measurement in Globalping. |
| [Create Ping Measurement](actions/create-ping-measurement.md) | POST | Creates a ping measurement in Globalping. |
| [Create TCP MTR Measurement](actions/create-tcp-mtr-measurement.md) | POST | Creates a TCP MTR measurement in Globalping. |
| [Create TCP Ping Measurement](actions/create-tcp-ping-measurement.md) | POST | Creates a TCP ping measurement in Globalping. |
| [Create TCP Traceroute Measurement](actions/create-tcp-traceroute-measurement.md) | POST | Creates a TCP traceroute measurement in Globalping. |
| [Create Traceroute Measurement](actions/create-traceroute-measurement.md) | POST | Creates a traceroute measurement in Globalping. |
| [Create UDP MTR Measurement](actions/create-udp-mtr-measurement.md) | POST | Creates a UDP MTR measurement in Globalping. |
| [Create UDP Traceroute Measurement](actions/create-udp-traceroute-measurement.md) | POST | Creates a UDP traceroute measurement in Globalping. |
| [Get Measurement](actions/get-measurement.md) | GET | Retrieves a Globalping measurement by ID. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Probes](actions/list-probes.md) | GET | Retrieves available Globalping probes. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Limits](actions/get-limits.md) | GET | Retrieves current Globalping usage limits. |

