# <img src="https://images.mindcloud.co/apps/icons/flexmail_1774459322048.png" alt="Flexmail logo" width="28" height="28"> Flexmail: Universal API

Manage contacts, opt-ins, imports, and webhooks in Flexmail

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flexmail/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flexmail.be
- **Vendor API docs:** https://api.flexmail.eu/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Flexmail. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from Flexmail. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from your Flexmail account. |
| [Replace Contact](actions/replace-contact.md) | PUT | Replaces an existing contact in Flexmail. |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT | Unsubscribes an existing contact from Flexmail communications. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Flexmail. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves available custom fields from Flexmail. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves available contact sources from Flexmail. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Submit Opt-In](actions/submit-opt-in.md) | POST | Creates an opt-in form submission in Flexmail. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Opt-In Forms](actions/list-opt-in-forms.md) | GET | Retrieves opt-in forms from your Flexmail account. |

### Import Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Import Records](actions/add-contact-import-records.md) | PUT | Adds records to a contact import in Flexmail. |
| [Create Contact Import](actions/create-contact-import.md) | POST | Creates a new contact import in Flexmail. |
| [Get Contact Import](actions/get-contact-import.md) | GET | Retrieves a contact import from Flexmail. |
| [Start Contact Import](actions/start-contact-import.md) | PUT | Starts a contact import in Flexmail. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves available contact segments from Flexmail. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Interest Subscription](actions/create-interest-subscription.md) | POST | Creates an interest subscription for a contact in Flexmail. |
| [Delete Interest Subscription](actions/delete-interest-subscription.md) | DELETE | Deletes an interest subscription from a contact in Flexmail. |
| [List Contact Interest Subscriptions](actions/list-contact-interest-subscriptions.md) | GET | Retrieves interest subscriptions for a contact from Flexmail. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Interests](actions/list-interests.md) | GET | Retrieves available contact interests from Flexmail. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Flexmail. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook endpoint from Flexmail. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook endpoint from Flexmail. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhook endpoints from Flexmail. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Flexmail. |

