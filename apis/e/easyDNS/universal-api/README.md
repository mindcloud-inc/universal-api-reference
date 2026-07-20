# <img src="https://images.mindcloud.co/apps/icons/big-bolt1-1_1781889126108.png" alt="easyDNS logo" width="28" height="28"> easyDNS: Universal API

Manage easyDNS domains, DNS zones, nameservers, mailmaps, user details, and service checks through the official EasyAPI REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyDNS/latest
- **Category:** IT Operations / DevOps
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://easydns.com
- **Vendor API docs:** https://docs.sandbox.rest.easydns.net:3001/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyDNS/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

