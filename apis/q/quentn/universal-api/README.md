# <img src="https://images.mindcloud.co/apps/icons/quentn_1773757571581.png" alt="Quentn logo" width="28" height="28"> Quentn: Universal API

Quentn integration for contacts, terms, custom fields, email, and campaign triggers using Quentn's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quentn/latest
- **Category:** Marketing
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quentn.com/
- **Vendor API docs:** https://help.quentn.com/hc/en-150/sections/4517317189009-API-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contact Comments](actions/list-contact-comments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments?connectionId=$CONNECTION_ID&contactId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Campaign Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact to Campaign](actions/add-contact-to-campaign.md) | POST |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Retrieve Contact](actions/retrieve-contact.md) | GET |  |
| [Retrieve Contacts by Mail](actions/retrieve-contacts-by-mail.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Comment](actions/add-contact-comment.md) | POST |  |
| [List Contact Comments](actions/list-contact-comments.md) | GET |  |
| [Update Contact Comment](actions/update-contact-comment.md) | PUT |  |

### Contact Term

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Terms](actions/list-contact-terms.md) | GET |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |
| [Retrieve Custom Field by ID](actions/retrieve-custom-field-by-id.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | POST |  |
| [Retrieve Email](actions/retrieve-email.md) | GET |  |

### Email Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST |  |

### Mail Sender

| Action | Method | Description |
| --- | --- | --- |
| [List Mail Senders](actions/list-mail-senders.md) | GET |  |

### Term

| Action | Method | Description |
| --- | --- | --- |
| [Create Term](actions/create-term.md) | POST |  |
| [List Terms](actions/list-terms.md) | GET |  |
| [Retrieve Term by ID](actions/retrieve-term-by-id.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

