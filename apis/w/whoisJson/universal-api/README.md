# <img src="https://images.mindcloud.co/apps/icons/whois-json_1776360218245.png" alt="WhoisJson logo" width="28" height="28"> WhoisJson: Universal API

Domain intelligence API for WHOIS, DNS, SSL certificate, domain availability, subdomain discovery, and reverse WHOIS lookups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whoisJson/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whoisjson.com
- **Vendor API docs:** https://whoisjson.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Whois Data](actions/get-whois-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whoisJson/latest/actions/get-whois-data?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Whois Data](actions/get-whois-data.md) | GET | Retrieves WHOIS data for a domain from WhoisJson. |

