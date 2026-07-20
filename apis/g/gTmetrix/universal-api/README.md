# <img src="https://images.mindcloud.co/apps/icons/g-tmetrix_1776279212606.png" alt="GTmetrix logo" width="28" height="28"> GTmetrix: Universal API

GTmetrix is a website performance testing platform for running page-speed tests, reading reports, managing tested pages, and retrieving performance artifacts through the GTmetrix REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gTmetrix/latest
- **Category:** IT Operations / Observability
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gtmetrix.com/
- **Vendor API docs:** https://gtmetrix.com/api/docs/2.0/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Status](actions/get-account-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gTmetrix/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Status](actions/get-account-status.md) | GET | Retrieves your current GTmetrix account status. |

