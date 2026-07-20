# <img src="https://images.mindcloud.co/apps/icons/i-p2proxy_1775162832034.png" alt="IP2Proxy logo" width="28" height="28"> IP2Proxy: Universal API

Detect proxies and inspect IP intelligence for IP addresses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iP2Proxy/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ip2location.com
- **Vendor API docs:** https://www.ip2location.com/web-service/ip2proxy

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Proxy Lookup](actions/get-proxy-lookup.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iP2Proxy/latest/actions/get-proxy-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET | Retrieves remaining web service credits from IP2Proxy. |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Proxy Lookup](actions/get-proxy-lookup.md) | GET | Retrieves proxy details for an IP address from IP2Proxy. |

