# <img src="https://images.mindcloud.co/apps/icons/wooxy_1775665270084.png" alt="Wooxy logo" width="28" height="28"> Wooxy: Universal API

Create, launch, and analyze multichannel marketing campaigns with AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wooxy/latest
- **Category:** Marketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wooxy.com
- **Vendor API docs:** https://wooxy.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Statistics](actions/get-message-statistics.md) | GET | Retrieves email message statistics from Wooxy. |
| [Send Batch Email](actions/send-batch-email.md) | POST | Sends a batch email through Wooxy. |
| [Send Batch Triggered Email](actions/send-batch-triggered-email.md) | POST | Sends batch triggered emails through Wooxy. |
| [Send Email](actions/send-email.md) | POST | Sends an email through your Wooxy account. |
| [Send Triggered Email](actions/send-triggered-email.md) | POST | Sends a triggered email through Wooxy. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your current Wooxy account information. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Variable](actions/create-account-variable.md) | POST | Creates a new account variable in Wooxy. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Wooxy. |
| [Create Contact List Variable](actions/create-contact-list-variable.md) | POST | Creates a new contact list variable in Wooxy. |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Wooxy. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Wooxy. |
| [Delete Account Variable](actions/delete-account-variable.md) | DELETE | Deletes an existing account variable from Wooxy. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Wooxy. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Wooxy. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Wooxy. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from your Wooxy account. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Wooxy. |
| [Get Contact Mutation Request Status](actions/get-contact-mutation-request-status.md) | GET | Retrieves contact mutation request statuses from Wooxy. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from your Wooxy account. |
| [List Account Variables](actions/list-account-variables.md) | GET | Retrieves account variables from your Wooxy account. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Finds contact lists in your Wooxy account. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from your Wooxy account. |
| [Update Account Variable](actions/update-account-variable.md) | PUT | Updates an existing account variable in Wooxy. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Wooxy. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Wooxy. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Wooxy. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Wooxy. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from your Wooxy account. |
| [List Templates](actions/list-templates.md) | GET | Finds templates in your Wooxy account. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Wooxy. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a new domain in Wooxy. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Wooxy. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing domain from Wooxy. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Wooxy. |
| [Fire Event](actions/fire-event.md) | POST | Fires a custom event in Wooxy. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from your Wooxy account. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from your Wooxy account. |
| [List Domains](actions/list-domains.md) | GET | Finds domains in your Wooxy account. |
| [List Events](actions/list-events.md) | GET | Finds events in your Wooxy account. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Wooxy. |
| [Verify Domain](actions/verify-domain.md) | PUT | Verifies an existing domain in Wooxy. |

