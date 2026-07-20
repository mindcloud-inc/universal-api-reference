# <img src="https://images.mindcloud.co/apps/icons/sendcrux_1775167131790.png" alt="Sendcrux logo" width="28" height="28"> Sendcrux: Universal API

Sendcrux is an email marketing and cold outreach platform for managing lists, subscribers, campaigns, delivery events, and related account resources through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendcrux/latest
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendcrux.com
- **Vendor API docs:** https://api.sendbound.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Email Lists](actions/list-email-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/list-email-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Active Campaigns](actions/list-active-campaigns.md) | GET | Retrieves active campaigns from the Sendcrux account. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Sendcrux by UID. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Sendcrux. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses an existing campaign in Sendcrux. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Add Email List Field](actions/add-email-list-field.md) | POST | Creates a custom field for an email list in Sendcrux. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload Files](actions/upload-files.md) | POST | Uploads one or more files to Sendcrux. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List](actions/create-email-list.md) | POST | Creates a new email list in Sendcrux. |
| [Delete Email List](actions/delete-email-list.md) | DELETE | Deletes an email list from Sendcrux. |
| [Get Email List](actions/get-email-list.md) | GET | Retrieves an email list from Sendcrux by UID. |
| [List Email Lists](actions/list-email-lists.md) | GET | Retrieves a list of email lists from Sendcrux. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Send Abuse Notification](actions/send-abuse-notification.md) | POST | Creates an abuse notification event in Sendcrux. |
| [Send Bounce Notification](actions/send-bounce-notification.md) | POST | Creates a bounce notification event in Sendcrux. |
| [Send Delivery Notification](actions/send-delivery-notification.md) | POST | Creates a delivery notification event in Sendcrux. |
| [Send Failed Notification](actions/send-failed-notification.md) | POST | Creates a failed notification event in Sendcrux. |
| [Send Notification](actions/send-notification.md) | POST | Creates a notification event in Sendcrux. |
| [Send Spam Notification](actions/send-spam-notification.md) | POST | Creates a spam notification event in Sendcrux. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Generate Login Token](actions/generate-login-token.md) | POST | Creates a login token in Sendcrux. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribed Subscribers](actions/list-subscribed-subscribers.md) | GET | Retrieves subscribed subscribers from a Sendcrux email list. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscriber Tags](actions/add-subscriber-tags.md) | PUT | Updates a subscriber in Sendcrux by adding tags. |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in a Sendcrux email list. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from Sendcrux. |
| [Find Subscribers By Email](actions/find-subscribers-by-email.md) | GET | Finds subscribers in Sendcrux by email address. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Sendcrux by UID. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from a Sendcrux email list. |
| [Subscribe Subscriber to List](actions/subscribe-subscriber-to-list.md) | PUT | Updates a Sendcrux subscriber by subscribing them to a list. |
| [Unsubscribe Subscriber from List](actions/unsubscribe-subscriber-from-list.md) | PUT | Updates a Sendcrux subscriber by unsubscribing them from a list. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Sendcrux. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [List Subscriptions By Plan](actions/list-subscriptions-by-plan.md) | GET |  |

