# Nimble: Native API Reference

A consolidated summary of Nimble's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.nimble.com/developers/docs/
- **API base URL:** `https://app.nimble.com`

## Authentication

### API Key

Connect Nimble using a personal or account API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nimble.com/developers/docs/#tag/Authentication/API-requests-using-Access-Token)

## API conventions

Response data is read from `resources`. The total page count is read from `meta.pages`. The current page number is read from `meta.page`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Tags to Contact](actions/assign-tags-to-contact.md) | `PUT /api/v1/contacts/:contact_id/tags` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact-tags) |
| [Create Contact](actions/create-contact.md) | `POST /api/v1/contact` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/post-contact) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /api/v1/contacts/notes` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/post-contact-note) |
| [Create Deal](actions/create-deal.md) | `POST /api/v2/deals` | [docs](https://www.nimble.com/developers/docs/#tag/Deals/operation/create-new-deal) |
| [Create Draft Message](actions/create-draft-message.md) | `POST /api/v1/messages/drafts` | [docs](https://www.nimble.com/developers/docs/#tag/Messages/operation/post-message-draft) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v1/contact/:contact_id` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/delete-contact) |
| [Delete Contact Note](actions/delete-contact-note.md) | `DELETE /api/v1/contacts/notes/:note_id` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/delete-contact-note) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /api/v2/deals/:deal_id` | [docs](https://www.nimble.com/developers/docs/#tag/Deals/operation/delete-deal) |
| [Exit Lead from Pipeline Successfully](actions/exit-lead-from-pipeline-successfully.md) | `POST /api/v2/leads/:lead_id/:pipeline_id/successful` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/mark-lead-exited-successful) |
| [Exit Lead from Pipeline Unsuccessfully](actions/exit-lead-from-pipeline-unsuccessfully.md) | `POST /api/v2/leads/:lead_id/:pipeline_id/unsuccessful` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/mark-lead-exited-unsuccessfully) |
| [Get Contact](actions/get-contact.md) | `GET /api/v1/contact/:contact_id` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/get-contact) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/myself` | [docs](https://www.nimble.com/developers/docs/#tag/Users/operation/get-myself) |
| [Get Deal](actions/get-deal.md) | `GET /api/v2/deals/:deal_id` | [docs](https://www.nimble.com/developers/docs/#tag/Deals/operation/get-deal) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /api/v1/contact/:contact_id/notes` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contact-notes) |
| [List Contact Pipelines](actions/list-contact-pipelines.md) | `GET /api/v1/contacts/pipelines` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/list-available-contacts-pipelines) |
| [List Contact Proceedings](actions/list-contact-proceedings.md) | `GET /api/v1/contacts/:contact_id/proceedings` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contact-proceedings) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/contacts` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contacts) |
| [List Deal Pipelines](actions/list-deal-pipelines.md) | `GET /api/v2/deals/pipelines` | [docs](https://www.nimble.com/developers/docs/#tag/Deals-Pipelines/operation/list-deals-pipelines) |
| [List Deals](actions/list-deals.md) | `GET /api/v2/deals` | [docs](https://www.nimble.com/developers/docs/#tag/Deals/operation/list-user-deals) |
| [Move Lead To Pipeline Stage](actions/move-lead-to-pipeline-stage.md) | `POST /api/v2/leads/:lead_id/:pipeline_id/move` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts-Pipelines/operation/move-lead) |
| [Search Contacts by Identifiers](actions/search-contacts-by-identifiers.md) | `GET /api/v1/contacts` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contacts-for-identifiers) |
| [Update Contact](actions/update-contact.md) | `PUT /api/v1/contact/:contact_id` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact) |
| [Update Contact Note](actions/update-contact-note.md) | `PUT /api/v1/contacts/notes/:note_id` | [docs](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact-note) |
| [Update Deal](actions/update-deal.md) | `PUT /api/v2/deals/:deal_id` | [docs](https://www.nimble.com/developers/docs/#tag/Deals/operation/put-deal) |
