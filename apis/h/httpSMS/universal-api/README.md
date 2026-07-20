# <img src="https://images.mindcloud.co/apps/icons/http-sms_1776178645659.png" alt="httpSMS logo" width="28" height="28"> httpSMS: Universal API

Send, receive, and automate SMS with Android phones

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/httpSMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://httpsms.com
- **Vendor API docs:** https://api.httpsms.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/httpSMS/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&contact=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET |  |

