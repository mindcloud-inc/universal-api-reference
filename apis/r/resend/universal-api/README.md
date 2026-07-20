# <img src="https://images.mindcloud.co/apps/icons/resend-icon-black_1770823594778.png" alt="Resend logo" width="28" height="28"> Resend: Universal API

The best way to reach humans instead of spam folders.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/resend/latest
- **Category:** Marketing
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://resend.com
- **Vendor API docs:** https://resend.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API Keys](actions/list-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Resend. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from Resend. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API keys from Resend. |

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Delete Audience](actions/delete-audience.md) | DELETE | Deletes an existing audience from Resend. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Broadcasts](actions/list-broadcasts.md) | GET | Retrieves broadcasts from Resend. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Resend. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Resend. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Resend. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Resend. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Resend. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a new domain in Resend. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing domain from Resend. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Resend. |
| [Retrieve Domain](actions/retrieve-domain.md) | GET | Retrieves a domain from Resend. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing domain in Resend. |
| [Verify Domain](actions/verify-domain.md) | PUT | Triggers verification for an existing domain in Resend. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Email](actions/cancel-email.md) | PUT | Cancels a scheduled email in Resend. |
| [List Received Emails](actions/list-received-emails.md) | GET | Retrieves received emails from Resend. |
| [List Sent Emails](actions/list-sent-emails.md) | GET | Retrieves sent emails from Resend. |
| [Retrieve Email](actions/retrieve-email.md) | GET | Retrieves an email from Resend. |
| [Send Batch Emails](actions/send-batch-emails.md) | POST | Sends up to 100 emails in a Resend batch. |
| [Send Email](actions/send-email.md) | POST | Creates a new email in Resend. |
| [Update Email](actions/update-email.md) | PUT | Updates an existing email in Resend. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Audience](actions/create-audience.md) | POST | Creates a new audience in Resend. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from Resend. |
| [Retrieve Audience](actions/retrieve-audience.md) | GET | Retrieves an audience from Resend. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Resend. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Resend. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Resend. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Resend. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Resend. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Resend. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Resend. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Resend. |
| [Retrieve Webhook](actions/retrieve-webhook.md) | GET | Retrieves a webhook from Resend. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Resend. |

