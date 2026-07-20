# Mx Toolbox: Native API Reference

A consolidated summary of Mx Toolbox's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://knowledgebase.mxtoolbox.com/home/api
- **API base URL:** `https://api.mxtoolbox.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://knowledgebase.mxtoolbox.com/home/about-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Blocklist](actions/check-blocklist.md) | `GET /lookup/blocklist` | [docs](https://mxtoolbox.com/blocklists.aspx) |
| [Check DNS Servers](actions/check-dns-servers.md) | `GET /lookup/dns` | [docs](https://mxtoolbox.com/DNSCheck.aspx) |
| [Lookup A Record](actions/lookup-a-record.md) | `GET /lookup/a` | [docs](https://mxtoolbox.com/DnsLookup.aspx) |
| [Lookup AAAA Record](actions/lookup-aaaa-record.md) | `GET /lookup/aaaa` | [docs](https://mxtoolbox.com/IPv6.aspx) |
| [Lookup ASN Information](actions/lookup-asn-information.md) | `GET /lookup/asn` | [docs](https://mxtoolbox.com/asn.aspx) |
| [Lookup BIMI Record](actions/lookup-bimi-record.md) | `GET /lookup/bimi` | [docs](https://mxtoolbox.com/bimi.aspx) |
| [Lookup CNAME Record](actions/lookup-cname-record.md) | `GET /lookup/cname` | [docs](https://mxtoolbox.com/CnameLookup.aspx) |
| [Lookup DKIM Record](actions/lookup-dkim-record.md) | `GET /lookup/dkim` | [docs](https://mxtoolbox.com/dkim.aspx) |
| [Lookup DMARC Record](actions/lookup-dmarc-record.md) | `GET /lookup/dmarc` | [docs](https://mxtoolbox.com/dmarc.aspx) |
| [Lookup HTTP](actions/lookup-http.md) | `GET /lookup/http` | [docs](https://mxtoolbox.com/HTTPLookup.aspx) |
| [Lookup HTTPS](actions/lookup-https.md) | `GET /lookup/https` | [docs](https://mxtoolbox.com/HTTPSLookup.aspx) |
| [Lookup MTA-STS Record](actions/lookup-mta-sts-record.md) | `GET /lookup/mta-sts` | [docs](https://mxtoolbox.com/mta-sts.aspx) |
| [Lookup MX Records](actions/lookup-mx-records.md) | `GET /lookup/mx` | [docs](https://mxtoolbox.com/MXLookup.aspx) |
| [Lookup PTR Record](actions/lookup-ptr-record.md) | `GET /lookup/ptr` | [docs](https://mxtoolbox.com/ReverseLookup.aspx) |
| [Lookup SOA Record](actions/lookup-soa-record.md) | `GET /lookup/soa` | [docs](https://mxtoolbox.com/SOALookup.aspx) |
| [Lookup SPF Record](actions/lookup-spf-record.md) | `GET /lookup/spf` | [docs](https://mxtoolbox.com/spf.aspx) |
| [Lookup TCP Port](actions/lookup-tcp-port.md) | `GET /lookup/tcp` | [docs](https://mxtoolbox.com/TCPLookup.aspx) |
| [Lookup TXT Record](actions/lookup-txt-record.md) | `GET /lookup/txt` | [docs](https://mxtoolbox.com/TXTLookup.aspx) |
| [Lookup WHOIS](actions/lookup-whois.md) | `GET /lookup/whois` | [docs](https://mxtoolbox.com/Whois.aspx) |
| [Test SMTP](actions/test-smtp.md) | `GET /lookup/smtp` | [docs](https://mxtoolbox.com/diagnostic.aspx) |
