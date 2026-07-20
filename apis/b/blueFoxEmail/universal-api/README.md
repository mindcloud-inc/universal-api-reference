# <img src="https://images.mindcloud.co/apps/icons/bluefox-icon_1774895262684.png" alt="BlueFox Email logo" width="28" height="28"> BlueFox Email: Universal API

Send transactional, triggered, and campaign emails and manage contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blueFoxEmail/latest
- **Category:** Marketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bluefox.email
- **Vendor API docs:** https://bluefox.email/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subscribers](actions/list-subscribers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueFoxEmail/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&subscriberListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in BlueFox Email. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from BlueFox Email. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from BlueFox Email. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from BlueFox Email. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in BlueFox Email. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Send Transactional Email](actions/send-transactional-email.md) | POST | Sends a transactional email through BlueFox Email. |
| [Send Triggered Email](actions/send-triggered-email.md) | POST | Sends a triggered email through BlueFox Email. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Activate Subscription](actions/activate-subscription.md) | PUT | Activates a subscriber in a BlueFox Email list. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from a BlueFox Email list. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from a BlueFox Email list. |
| [Pause Subscription](actions/pause-subscription.md) | PUT | Pauses a subscriber in a BlueFox Email list. |
| [Subscribe](actions/subscribe.md) | POST | Subscribes a contact to a BlueFox Email list. |
| [Unsubscribe](actions/unsubscribe.md) | PUT | Unsubscribes a contact from a BlueFox Email list. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates a subscriber in a BlueFox Email list. |

