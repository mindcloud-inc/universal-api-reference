# <img src="https://images.mindcloud.co/apps/icons/push-call-me_1774454421674.png" alt="PushCallMe logo" width="28" height="28"> PushCallMe: Universal API

Trigger short notification phone calls and retrieve call outcomes through the PushCall HTTP API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushCallMe/latest
- **Category:** Support / Contact Center
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pushcall.me
- **Vendor API docs:** https://pushcall.me/docs/phone-call-via-http-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Call Status](actions/get-call-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Status](actions/get-call-status.md) | GET | Retrieves call status details from PushCallMe. |
| [Make Phone Call](actions/make-phone-call.md) | POST | Creates a new phone call in PushCallMe. |

