# <img src="https://images.mindcloud.co/apps/icons/texting-house_1775145881262.png" alt="TextingHouse logo" width="28" height="28"> TextingHouse: Universal API

Send SMS, track delivery, and monitor TextingHouse credit balance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/textingHouse/latest
- **Category:** Communication / Team Messaging
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.textinghouse.com/en/api-sms-http
- **Vendor API docs:** https://www.textinghouse.com/en/api-sms-http/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textingHouse/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Status By API Message ID](actions/get-sms-status-by-api-message-id.md) | GET | Retrieves TextingHouse SMS status by API message ID. |
| [Get SMS Status By Client Message ID](actions/get-sms-status-by-client-message-id.md) | GET | Retrieves TextingHouse SMS status by client message ID. |
| [Send Commercial SMS](actions/send-commercial-sms.md) | POST | Creates a commercial SMS in TextingHouse. |
| [Send Service SMS](actions/send-service-sms.md) | POST | Creates a service SMS in TextingHouse. |
| [Send Test SMS To 999](actions/send-test-sms-to999.md) | POST | Creates a test SMS to 999 in TextingHouse. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves the current TextingHouse credit balance. |

