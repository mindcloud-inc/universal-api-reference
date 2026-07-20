# <img src="https://images.mindcloud.co/apps/icons/expert-texting_1775594736134.png" alt="ExpertTexting logo" width="28" height="28"> ExpertTexting: Universal API

ExpertTexting lets users send SMS and MMS messages, check delivery status, read unread inbox replies, and view account balance through the provider's published REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/expertTexting/latest
- **Category:** Communication / Team Messaging
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.experttexting.com
- **Vendor API docs:** https://www.experttexting.com/appv2/documentation/index/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Balance](actions/check-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Check Message Status](actions/check-message-status.md) | GET | Retrieves message status from ExpertTexting by message ID. |
| [List Unread Inbox Messages](actions/list-unread-inbox-messages.md) | GET | Retrieves unread inbox messages from ExpertTexting. |
| [Send MMS](actions/send-mms.md) | POST | Creates an MMS message in ExpertTexting. |
| [Send SMS](actions/send-sms.md) | POST | Creates an SMS message in ExpertTexting. |
| [Send Unicode SMS](actions/send-unicode-sms.md) | POST | Creates a Unicode SMS message in ExpertTexting. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Retrieves account balance from ExpertTexting. |

