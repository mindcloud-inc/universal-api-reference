# <img src="https://images.mindcloud.co/apps/icons/mailtrap_1774552261141.png" alt="Mailtrap logo" width="28" height="28"> Mailtrap: Universal API

Mailtrap operational API wrapper for sending domains, stats, contacts, contact lists, and templates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailtrap/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailtrap.io
- **Vendor API docs:** https://docs.mailtrap.io/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Permissions](actions/list-permissions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/list-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Mailtrap. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Mailtrap. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Mailtrap. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Mailtrap. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST | Creates a new email template in Mailtrap. |
| [Delete Email Template](actions/delete-email-template.md) | DELETE | Deletes an existing email template from Mailtrap. |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template from Mailtrap. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from Mailtrap. |
| [Update Email Template](actions/update-email-template.md) | PUT | Updates an existing email template in Mailtrap. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Sending Domain](actions/create-sending-domain.md) | POST | Creates a new sending domain in Mailtrap. |
| [Delete Sending Domain](actions/delete-sending-domain.md) | DELETE | Deletes an existing sending domain from Mailtrap. |
| [Get Sending Domain](actions/get-sending-domain.md) | GET | Retrieves a sending domain from Mailtrap. |
| [List Sending Domains](actions/list-sending-domains.md) | GET | Retrieves sending domains from Mailtrap. |
| [Send Setup Instructions](actions/send-setup-instructions.md) | POST | Sends sending domain setup instructions from Mailtrap. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in Mailtrap. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from Mailtrap. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Mailtrap. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Mailtrap. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in Mailtrap. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Permissions](actions/list-permissions.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Sending Stats](actions/get-sending-stats.md) | GET | Retrieves sending stats from Mailtrap. |
| [Get Sending Stats by Categories](actions/get-sending-stats-by-categories.md) | GET | Retrieves Mailtrap sending stats by category. |
| [Get Sending Stats by Date](actions/get-sending-stats-by-date.md) | GET | Retrieves Mailtrap sending stats by date. |
| [Get Sending Stats by Domains](actions/get-sending-stats-by-domains.md) | GET | Retrieves Mailtrap sending stats by domain. |

