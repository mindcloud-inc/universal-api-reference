# SureContact: Native API Reference

A consolidated summary of SureContact's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.surecontact.com/docs
- **API base URL:** `https://api.surecontact.com`

## Authentication

### API Key

Connect with a SureContact API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.surecontact.com/docs#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 15). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts to List](actions/add-contacts-to-list.md) | `POST api/v1/public/lists/:list_uuid/contacts/add` | [docs](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--contacts-add) |
| [Add Contacts to Tag](actions/add-contacts-to-tag.md) | `POST api/v1/public/tags/:tag_uuid/contacts/add` | [docs](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags--tag_uuid--contacts-add) |
| [Copy List](actions/copy-list.md) | `POST api/v1/public/lists/:list_uuid/copy` | [docs](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--copy) |
| [Create List](actions/create-list.md) | `POST api/v1/public/lists` | [docs](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists) |
| [Create Note](actions/create-note.md) | `POST api/v1/public/contacts/:contact_uuid/notes` | [docs](https://api.surecontact.com/docs#contact-notes-POSTapi-v1-public-contacts--contact_uuid--notes) |
| [Create Tag](actions/create-tag.md) | `POST api/v1/public/tags` | [docs](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags) |
| [Delete Contact](actions/delete-contact.md) | `DELETE api/v1/public/contacts/:contact_uuid` | [docs](https://api.surecontact.com/docs#contact-management-DELETEapi-v1-public-contacts--contact_uuid-) |
| [Duplicate Campaign](actions/duplicate-campaign.md) | `POST api/v1/public/campaigns/:campaign_uuid/duplicate` | [docs](https://api.surecontact.com/docs#endpoints-POSTapi-v1-public-campaigns--campaign_uuid--duplicate) |
| [Find Contact by Email](actions/find-contact-by-email.md) | `GET api/v1/public/contacts/email/:email` | [docs](https://api.surecontact.com/docs#contact-management-GETapi-v1-public-contacts-email--email-) |
| [Find or Create Contact](actions/find-or-create-contact.md) | `POST api/v1/public/contacts` | [docs](https://api.surecontact.com/docs#contact-management-POSTapi-v1-public-contacts) |
| [Get Campaign](actions/get-campaign.md) | `GET api/v1/public/campaigns/:campaign_uuid` | [docs](https://api.surecontact.com/docs#endpoints-GETapi-v1-public-campaigns--campaign_uuid-) |
| [Get Contact](actions/get-contact.md) | `GET api/v1/public/contacts/:contact_uuid` | [docs](https://api.surecontact.com/docs#contact-management-GETapi-v1-public-contacts--contact_uuid-) |
| [Get List](actions/get-list.md) | `GET api/v1/public/lists/:list_uuid` | [docs](https://api.surecontact.com/docs#list-management-GETapi-v1-public-lists--list_uuid-) |
| [Get Reports Overview](actions/get-reports-overview.md) | `GET api/v1/public/reports/overview` | [docs](https://api.surecontact.com/docs#reports-GETapi-v1-public-reports-overview) |
| [Get Tag](actions/get-tag.md) | `GET api/v1/public/tags/:tag_uuid` | [docs](https://api.surecontact.com/docs#tag-management-GETapi-v1-public-tags--tag_uuid-) |
| [List Campaigns](actions/list-campaigns.md) | `GET api/v1/public/campaigns` | [docs](https://api.surecontact.com/docs#endpoints-GETapi-v1-public-campaigns) |
| [List Contacts](actions/list-contacts.md) | `GET api/v1/public/contacts` | [docs](https://api.surecontact.com/docs#contact-management-GETapi-v1-public-contacts) |
| [List Contacts for List](actions/list-contacts-for-list.md) | `GET api/v1/public/lists/:list_uuid/contacts` | [docs](https://api.surecontact.com/docs#list-management-GETapi-v1-public-lists--list_uuid--contacts) |
| [List Contacts for Tag](actions/list-contacts-for-tag.md) | `GET api/v1/public/tags/:tag_uuid/contacts` | [docs](https://api.surecontact.com/docs#tag-management-GETapi-v1-public-tags--tag_uuid--contacts) |
| [List Lists](actions/list-lists.md) | `GET api/v1/public/lists` | [docs](https://api.surecontact.com/docs#list-management-GETapi-v1-public-lists) |
| [List Notes](actions/list-notes.md) | `GET api/v1/public/contacts/:contact_uuid/notes` | [docs](https://api.surecontact.com/docs#contact-notes-GETapi-v1-public-contacts--contact_uuid--notes) |
| [List Tags](actions/list-tags.md) | `GET api/v1/public/tags` | [docs](https://api.surecontact.com/docs#tag-management-GETapi-v1-public-tags) |
| [Remove Contacts from List](actions/remove-contacts-from-list.md) | `POST api/v1/public/lists/:list_uuid/contacts/remove` | [docs](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists--list_uuid--contacts-remove) |
| [Remove Contacts from Tag](actions/remove-contacts-from-tag.md) | `POST api/v1/public/tags/:tag_uuid/contacts/remove` | [docs](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags--tag_uuid--contacts-remove) |
| [Update Contact](actions/update-contact.md) | `PUT api/v1/public/contacts/:contact_uuid` | [docs](https://api.surecontact.com/docs#contact-management-PUTapi-v1-public-contacts--contact_uuid-) |
| [Update Contact Status](actions/update-contact-status.md) | `PATCH api/v1/public/contacts/:contact_uuid/status` | [docs](https://api.surecontact.com/docs#contact-management-PATCHapi-v1-public-contacts--contact_uuid--status) |
| [Update List](actions/update-list.md) | `PUT api/v1/public/lists/:list_uuid` | [docs](https://api.surecontact.com/docs#list-management-PUTapi-v1-public-lists--list_uuid-) |
| [Update Note](actions/update-note.md) | `PUT api/v1/public/notes/:note_uuid` | [docs](https://api.surecontact.com/docs#contact-notes-PUTapi-v1-public-notes--note_uuid-) |
| [Update Tag](actions/update-tag.md) | `PUT api/v1/public/tags/:tag_uuid` | [docs](https://api.surecontact.com/docs#tag-management-PUTapi-v1-public-tags--tag_uuid-) |
| [Upsert Contact](actions/upsert-contact.md) | `POST api/v1/public/contacts/upsert` | [docs](https://api.surecontact.com/docs#contact-management-POSTapi-v1-public-contacts-upsert) |
