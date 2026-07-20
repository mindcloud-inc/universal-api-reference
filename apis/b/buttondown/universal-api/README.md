# <img src="https://images.mindcloud.co/apps/icons/buttondown_1773944518839.png" alt="Buttondown logo" width="28" height="28"> Buttondown: Universal API

Manage Buttondown newsletters, subscribers, emails, automations, and webhooks through the official Buttondown API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buttondown/latest
- **Category:** Communication / Email Communications
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://buttondown.com
- **Vendor API docs:** https://docs.buttondown.com/api-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Newsletters](actions/list-newsletters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-newsletters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Email](actions/create-draft-email.md) | POST | Creates a draft email in Buttondown. |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an existing email from Buttondown. |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails from Buttondown. |
| [Retrieve Email](actions/retrieve-email.md) | GET | Retrieves an email from Buttondown. |
| [Send Draft Email](actions/send-draft-email.md) | POST | Sends a draft email from Buttondown to specific recipients. |
| [Update Draft Email](actions/update-draft-email.md) | PUT | Updates an existing draft email in Buttondown. |

### Newsletter

| Action | Method | Description |
| --- | --- | --- |
| [List Newsletters](actions/list-newsletters.md) | GET | Retrieves newsletters from Buttondown. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber](actions/create-subscriber.md) | POST | Creates a new subscriber in Buttondown. |
| [Delete Subscriber](actions/delete-subscriber.md) | DELETE | Deletes an existing subscriber from Buttondown. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from Buttondown. |
| [Retrieve Subscriber](actions/retrieve-subscriber.md) | GET | Retrieves a subscriber from Buttondown by ID or email address. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in Buttondown. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Buttondown. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Buttondown. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Buttondown. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves a webhook from Buttondown. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Buttondown. |

### Webhook Attempt

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Attempts](actions/list-webhook-attempts.md) | GET | Retrieves webhook attempts from Buttondown. |
| [Test Webhook](actions/test-webhook.md) | POST | Sends a test event to a Buttondown webhook. |

