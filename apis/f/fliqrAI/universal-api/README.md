# <img src="https://images.mindcloud.co/apps/icons/1716795693-fliqr-ai-qornhlvock8xelta7uzn4odfico9o2pj6q1s3xi45c_1776715430123.png" alt="Fliqr AI logo" width="28" height="28"> Fliqr AI: Universal API

Manage Fliqr contacts, flows, tags, pipelines, and ecommerce

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fliqrAI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fliqr.ai/
- **Vendor API docs:** https://docs.fliqr.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Business Account Details](actions/get-business-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/get-business-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Admin

| Action | Method | Description |
| --- | --- | --- |
| [List Account Admins](actions/list-account-admins.md) | GET | Retrieves account admins from Fliqr AI. |

### Bot Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Bot Field Value](actions/get-bot-field-value.md) | GET |  |
| [Set Bot Field Value](actions/set-bot-field-value.md) | PUT |  |

### Business Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Account Details](actions/get-business-account-details.md) | GET | Retrieves business account details from Fliqr AI. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Fliqr AI. |
| [Find Contacts By Custom Field](actions/find-contacts-by-custom-field.md) | GET |  |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Fliqr AI. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Custom Field](actions/create-account-custom-field.md) | POST |  |
| [Get Account Custom Field](actions/get-account-custom-field.md) | GET |  |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | GET |  |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET |  |
| [Set Contact Custom Field](actions/set-contact-custom-field.md) | PUT |  |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Account Flows](actions/list-account-flows.md) | GET | Retrieves account flows from Fliqr AI. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Flow To Contact](actions/send-flow-to-contact.md) | POST | Sends a flow to a contact in Fliqr AI. |
| [Send Text Message To Contact](actions/send-text-message-to-contact.md) | POST | Sends a text message to a contact in Fliqr AI. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Fliqr AI. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | POST | Creates a tag assignment for a contact in Fliqr AI. |
| [Create Account Tag](actions/create-account-tag.md) | POST | Creates a new account tag in Fliqr AI. |
| [Find Account Tag By Name](actions/find-account-tag-by-name.md) | GET | Finds an account tag in Fliqr AI by name. |
| [Get Account Tag](actions/get-account-tag.md) | GET | Retrieves an account tag from Fliqr AI. |
| [List Account Tags](actions/list-account-tags.md) | GET | Retrieves account tags from Fliqr AI. |
| [List Contact Tags](actions/list-contact-tags.md) | GET | Retrieves contact tags from Fliqr AI. |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | DELETE | Deletes a tag assignment from a contact in Fliqr AI. |

