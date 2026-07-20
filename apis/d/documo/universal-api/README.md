# <img src="https://images.mindcloud.co/apps/icons/documo_1774380663931.png" alt="Documo logo" width="28" height="28"> Documo: Universal API

Send faxes and manage Documo contacts, webhooks, and metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documo/latest
- **Category:** Support / Contact Center
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.documo.com/
- **Vendor API docs:** https://docs.documo.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Documo. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API key records from Documo. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Documo. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Documo. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from your Documo account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Documo. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Archive Custom Field](actions/archive-custom-field.md) | PUT | Archives an existing custom field in Documo. |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in Documo. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from Documo. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom field records from Documo. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Documo. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Documo. |
| [Get Folder Info](actions/get-folder-info.md) | GET | Retrieves folder details and counts from Documo. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Fax](actions/send-fax.md) | POST | Creates a new fax message in Documo. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Validate Fax Number](actions/validate-fax-number.md) | GET | Validates a fax number in Documo. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Documo. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Documo. |
| [List Tags](actions/list-tags.md) | GET | Retrieves available tag records from Documo. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Cover Pages](actions/list-cover-pages.md) | GET | Retrieves cover page templates from Documo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from Documo. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Documo. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Documo. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook endpoint records from Documo. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Documo. |

