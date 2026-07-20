# <img src="https://images.mindcloud.co/apps/icons/s-msvio_1776111383536.png" alt="SMSVio logo" width="28" height="28"> SMSVio: Universal API

SMSVio API wrapper for SMS messaging and account balance checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSVio/latest
- **Category:** Communication / Team Messaging
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smsvio.cz/
- **Vendor API docs:** https://www.smsvio.cz/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Credits](actions/get-account-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/get-account-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Delete SMS](actions/delete-sms.md) | DELETE |  |
| [Get Account Credits](actions/get-account-credits.md) | GET |  |
| [Get SMS Details](actions/get-sms-details.md) | GET |  |
| [Send SMS](actions/send-sms.md) | POST |  |
| [Send SMS to Multiple Numbers](actions/send-sms-to-multiple-numbers.md) | POST |  |

