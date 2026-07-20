# <img src="https://images.mindcloud.co/apps/icons/mobile-text-alerts_1774019350767.png" alt="Mobile Text Alerts logo" width="28" height="28"> Mobile Text Alerts: Universal API

Send and manage SMS messaging through Mobile Text Alerts using a bearer API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mobileTextAlerts/latest
- **Category:** Communication / Team Messaging
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mobile-text-alerts.com
- **Vendor API docs:** https://developers.mobile-text-alerts.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Api Key Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Retrieves API key verification details from Mobile Text Alerts. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [List Deliveries](actions/list-deliveries.md) | GET | Retrieves message deliveries from Mobile Text Alerts. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Creates a message in Mobile Text Alerts. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Mobile Text Alerts. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from Mobile Text Alerts. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Finds a subscriber in Mobile Text Alerts by ID, number, or email. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from Mobile Text Alerts. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Mobile Text Alerts. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Mobile Text Alerts. |

