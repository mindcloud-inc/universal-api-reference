# <img src="https://images.mindcloud.co/apps/icons/s-ms8io_1776111375010.png" alt="SMS8.io logo" width="28" height="28"> SMS8.io: Universal API

SMS8.io through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMS8io/latest
- **Category:** Communication / Team Messaging
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sms8.io/
- **Vendor API docs:** https://sms8.io/sms8-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Message Status](actions/get-message-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-message-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get DLR Status](actions/get-dlr-status.md) | GET |  |
| [Get Message Status](actions/get-message-status.md) | GET |  |
| [Send SMS](actions/send-sms.md) | POST |  |

