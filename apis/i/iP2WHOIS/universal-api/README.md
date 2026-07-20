# <img src="https://images.mindcloud.co/apps/icons/i-p2whois_1774455688975.png" alt="IP2WHOIS logo" width="28" height="28"> IP2WHOIS: Universal API

Lookup domain WHOIS records and hosted domains by IP

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iP2WHOIS/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ip2whois.com/
- **Vendor API docs:** https://www.ip2location.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Domain WHOIS](actions/lookup-domain-whois.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2WHOIS/latest/actions/lookup-domain-whois?connectionId=$CONNECTION_ID&domain=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Hosted Domain Result

| Action | Method | Description |
| --- | --- | --- |
| [List Hosted Domains by IP](actions/list-hosted-domains-by-ip.md) | GET | Finds hosted domains in IP2WHOIS by IP address. |

### Whois Record

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Domain WHOIS](actions/lookup-domain-whois.md) | GET | Retrieves domain WHOIS details from IP2WHOIS. |

