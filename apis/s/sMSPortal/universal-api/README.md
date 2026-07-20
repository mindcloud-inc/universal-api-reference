# <img src="https://images.mindcloud.co/apps/icons/s-msportal_1774285607018.png" alt="SMSPortal logo" width="28" height="28"> SMSPortal: Universal API

Send and manage SMS messages, replies, and delivery workflows through SMSPortal's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSPortal/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smsportal.com/
- **Vendor API docs:** https://docs.smsportal.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Balance](actions/retrieve-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Balance](actions/retrieve-balance.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Messages](actions/send-messages.md) | POST |  |

