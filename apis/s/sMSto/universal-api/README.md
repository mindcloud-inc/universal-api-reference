# <img src="https://images.mindcloud.co/apps/icons/s-msto_1774540409313.png" alt="SMS.to logo" width="28" height="28"> SMS.to: Universal API

SMS.to: Send, manage, and track SMS, Viber, and campaign messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMSto/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sms.to
- **Vendor API docs:** https://developers.sms.to/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Last Message](actions/get-last-message.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Campaign Message](actions/estimate-campaign-message.md) | GET | Retrieves a cost estimate for a bulk SMS campaign. |
| [Estimate Campaign Viber](actions/estimate-campaign-viber.md) | GET | Retrieves a cost estimate for a Viber campaign. |
| [Estimate List Message](actions/estimate-list-message.md) | GET | Retrieves a cost estimate for an SMS list campaign. |
| [Estimate Personalized Message](actions/estimate-personalized-message.md) | GET | Retrieves a cost estimate for personalized SMS messages. |
| [Get Campaign by ID](actions/get-campaign-by-id.md) | GET | Retrieves a campaign by ID from SMS.to. |
| [Get Last Campaign](actions/get-last-campaign.md) | GET | Retrieves the most recent campaign from SMS.to. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves sent SMS campaigns from SMS.to. |
| [Schedule Sending Messages](actions/schedule-sending-messages.md) | POST | Schedules personalized SMS messages for later delivery in SMS.to. |
| [Schedule Sending Viber Messages](actions/schedule-sending-viber-messages.md) | POST | Schedules personalized Viber messages for later delivery. |
| [Send Campaign Message](actions/send-campaign-message.md) | POST | Sends an SMS campaign to multiple recipients in SMS.to. |
| [Send Campaign Viber](actions/send-campaign-viber.md) | POST | Sends a Viber campaign to multiple recipients in SMS.to. |
| [Send Message to a List or Multiple List in Array](actions/send-message-to-a-list-or-multiple-list-in-array.md) | POST | Sends an SMS message to one or more lists. |
| [Send Personalized Messages](actions/send-personalized-messages.md) | POST | Sends personalized SMS messages to multiple recipients. |
| [Send Viber to a List/s](actions/send-viber-to-a-lists.md) | POST | Sends a Viber message to one or more lists. |

### Flash Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Flash Message](actions/send-flash-message.md) | POST | Sends a single flash SMS message through SMS.to. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Single Message](actions/estimate-single-message.md) | GET | Retrieves a cost estimate for a single SMS message. |
| [Estimate Single Message Legacy GET](actions/estimate-single-message-legacy-get.md) | GET | Retrieves a cost estimate for a single SMS message using SMS.to's legacy endpoint. |
| [Estimate Single Viber Message](actions/estimate-single-viber-message.md) | GET | Retrieves a cost estimate for a single Viber message. |
| [Get Last Message](actions/get-last-message.md) | GET | Retrieves the most recent sent message from SMS.to. |
| [Get Message by ID](actions/get-message-by-id.md) | GET | Retrieves a sent message by ID from SMS.to. |
| [List Messages](actions/list-messages.md) | GET | Retrieves sent SMS messages from SMS.to. |
| [Send Single Message](actions/send-single-message.md) | POST | Sends a single SMS message through SMS.to. |
| [Send Viber Message](actions/send-viber-message.md) | POST | Sends a single Viber message through SMS.to. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Monthly Usage Report](actions/monthly-usage-report.md) | GET | Retrieves a monthly usage report from SMS.to. |

