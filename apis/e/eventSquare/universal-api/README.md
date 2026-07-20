# <img src="https://images.mindcloud.co/apps/icons/unnamed-6_1774455875918.png" alt="EventSquare logo" width="28" height="28"> EventSquare: Universal API

EventSquare is an event management platform for ticketing, registration, attendee engagement, and automation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventSquare/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eventsquare.co
- **Vendor API docs:** https://api.eventsquare.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Make Account](actions/get-make-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/get-make-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Make Account](actions/get-make-account.md) | GET | Retrieves the connected Make account from EventSquare. |
| [Get Zapier Account](actions/get-zapier-account.md) | GET | Retrieves the connected Zapier account from EventSquare. |

### Trigger Example

| Action | Method | Description |
| --- | --- | --- |
| [List Make Trigger Examples](actions/list-make-trigger-examples.md) | GET | Retrieves Make trigger examples from EventSquare. |
| [List Zapier Trigger Examples](actions/list-zapier-trigger-examples.md) | GET | Retrieves Zapier trigger examples from EventSquare. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Delete Make Webhook](actions/delete-make-webhook.md) | DELETE | Deletes a Make webhook from EventSquare. |
| [Delete Zapier Webhook](actions/delete-zapier-webhook.md) | DELETE | Deletes a Zapier webhook from EventSquare. |
| [Register Make Webhook](actions/register-make-webhook.md) | POST | Registers a Make webhook in EventSquare. |
| [Register Zapier Webhook](actions/register-zapier-webhook.md) | POST | Registers a Zapier webhook in EventSquare. |

