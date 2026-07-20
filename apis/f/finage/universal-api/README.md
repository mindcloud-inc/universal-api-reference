# <img src="https://images.mindcloud.co/apps/icons/finage_1776279936435.png" alt="Finage logo" width="28" height="28"> Finage: Universal API

Retrieve market data, fundamentals, news, and indicators across assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finage/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://finage.co.uk
- **Vendor API docs:** https://finage.co.uk/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Market Status](actions/get-market-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finage/latest/actions/get-market-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Market Status](actions/get-market-status.md) | GET | Retrieves market status from Finage. |

