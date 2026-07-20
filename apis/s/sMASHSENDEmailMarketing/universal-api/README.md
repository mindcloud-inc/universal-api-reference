# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1774906234237.png" alt="SMASHSEND Email Marketing logo" width="28" height="28"> SMASHSEND Email Marketing: Universal API

Create campaigns, automate journeys, send emails, and manage contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sMASHSENDEmailMarketing/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smashsend.com/
- **Vendor API docs:** https://smashsend.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMASHSENDEmailMarketing/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET | Validates a SMASHSEND API key and returns its details. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | POST | Creates or updates a contact in SMASHSEND by email. |
| [Delete Contact By Email](actions/delete-contact-by-email.md) | DELETE | Deletes a contact from SMASHSEND by email address. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact by ID from SMASHSEND. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your SMASHSEND workspace. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds a contact in SMASHSEND by email address. |

### Contact Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Property](actions/create-contact-property.md) | POST | Creates a new contact property in SMASHSEND. |
| [Delete Contact Property](actions/delete-contact-property.md) | DELETE | Deletes a contact property from SMASHSEND. |
| [Get Contact Property](actions/get-contact-property.md) | GET | Retrieves a contact property by ID from SMASHSEND. |
| [List Contact Properties](actions/list-contact-properties.md) | GET | Retrieves contact properties from your SMASHSEND workspace. |
| [Update Contact Property](actions/update-contact-property.md) | PUT | Updates an existing contact property in SMASHSEND. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST | Tracks a single contact event in SMASHSEND. |
| [Track Events Batch](actions/track-events-batch.md) | POST | Tracks multiple contact events in SMASHSEND in one batch. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in SMASHSEND. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from SMASHSEND. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook by ID from SMASHSEND. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your SMASHSEND workspace. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in SMASHSEND. |

