# <img src="https://images.mindcloud.co/apps/icons/big-mailer_1774377207752.png" alt="BigMailer logo" width="28" height="28"> BigMailer: Universal API

Manage brands, contacts, lists, templates, and email campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigMailer/latest
- **Category:** Communication / Email Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bigmailer.io/
- **Vendor API docs:** https://docs.bigmailer.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Brands](actions/list-brands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/list-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | GET | Retrieves a brand from your BigMailer account. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from your BigMailer account. |
| [Update Brand](actions/update-brand.md) | PUT | Updates an existing brand in BigMailer. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from your BigMailer account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in a BigMailer brand. |
| [Create or Update Contact](actions/create-or-update-contact.md) | PUT | Creates a new contact in a BigMailer brand, or updates an existing one that matches the email address. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from a BigMailer brand. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from a BigMailer brand. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a BigMailer brand. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in a BigMailer brand. |

### Contactbatch

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Batch Status](actions/get-contact-batch-status.md) | GET | Retrieves the status of a contact batch from a BigMailer brand. |
| [Upload Contact Batch](actions/upload-contact-batch.md) | POST | Uploads a batch of contacts to create or update asynchronously in a BigMailer brand. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in a BigMailer brand. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes a field from a BigMailer brand. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from a BigMailer brand. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from a BigMailer brand. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in a BigMailer brand. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in a BigMailer brand. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes a list from BigMailer while keeping contacts intact. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from a BigMailer brand. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from a BigMailer brand. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in a BigMailer brand. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in a BigMailer brand. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from a BigMailer brand. |

