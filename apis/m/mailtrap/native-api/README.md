# Mailtrap: Native API Reference

A consolidated summary of Mailtrap's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.mailtrap.io/developers
- **API base URL:** `https://mailtrap.io/api/accounts/:account_id`

## Authentication

### Mailtrap API Token

Authenticate Mailtrap requests with an account-level API token. Mailtrap accepts Api-Token or Authorization: Bearer.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mailtrap.io/developers/authentication)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `number` | yes |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contacts) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contacts/lists` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contact-lists) |
| [Create Email Template](actions/create-email-template.md) | `POST /email_templates` | [docs](https://docs.mailtrap.io/developers/management/templates) |
| [Create Sending Domain](actions/create-sending-domain.md) | `POST /sending_domains` | [docs](https://docs.mailtrap.io/developers/management/sending-domains) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{contact_identifier}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contacts) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contacts/lists/{list_id}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contact-lists) |
| [Delete Email Template](actions/delete-email-template.md) | `DELETE /email_templates/{email_template_id}` | [docs](https://docs.mailtrap.io/developers/management/templates) |
| [Delete Sending Domain](actions/delete-sending-domain.md) | `DELETE /sending_domains/{sending_domain_id}` | [docs](https://docs.mailtrap.io/developers/management/sending-domains) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{contact_identifier}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contacts) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contacts/lists/{list_id}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contact-lists) |
| [Get Email Template](actions/get-email-template.md) | `GET /email_templates/{email_template_id}` | [docs](https://docs.mailtrap.io/developers/management/templates) |
| [Get Sending Domain](actions/get-sending-domain.md) | `GET /sending_domains/{sending_domain_id}` | [docs](https://docs.mailtrap.io/developers/management/sending-domains) |
| [Get Sending Stats](actions/get-sending-stats.md) | `GET /stats` | [docs](https://docs.mailtrap.io/developers/management/stats) |
| [Get Sending Stats by Categories](actions/get-sending-stats-by-categories.md) | `GET /stats/categories` | [docs](https://docs.mailtrap.io/developers/management/stats) |
| [Get Sending Stats by Date](actions/get-sending-stats-by-date.md) | `GET /stats/date` | [docs](https://docs.mailtrap.io/developers/management/stats) |
| [Get Sending Stats by Domains](actions/get-sending-stats-by-domains.md) | `GET /stats/domains` | [docs](https://docs.mailtrap.io/developers/management/stats) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contacts/lists` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contact-lists) |
| [List Email Templates](actions/list-email-templates.md) | `GET /email_templates` | [docs](https://docs.mailtrap.io/developers/management/templates) |
| [List Permissions](actions/list-permissions.md) | `GET /permissions` | [docs](https://docs.mailtrap.io/developers/account-management/overview) |
| [List Sending Domains](actions/list-sending-domains.md) | `GET /sending_domains` | [docs](https://docs.mailtrap.io/developers/management/sending-domains) |
| [Send Setup Instructions](actions/send-setup-instructions.md) | `POST /sending_domains/{sending_domain_id}/send_setup_instructions` | [docs](https://docs.mailtrap.io/developers/management/sending-domains) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{contact_identifier}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contacts) |
| [Update Contact List](actions/update-contact-list.md) | `PATCH /contacts/lists/{list_id}` | [docs](https://docs.mailtrap.io/developers/promotional/contacts/contact-lists) |
| [Update Email Template](actions/update-email-template.md) | `PATCH /email_templates/{email_template_id}` | [docs](https://docs.mailtrap.io/developers/management/templates) |
