# DealMachine: Native API Reference

A consolidated summary of DealMachine's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.dealmachine.com/
- **API base URL:** `https://api.dealmachine.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.dealmachine.com/en/articles/10099784-how-to-use-the-dealmachine-api)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `after` in the query string as the pagination cursor.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | `POST /public/v1/leads/` | [docs](https://docs.dealmachine.com/) |
| [Add Lead To Lists](actions/add-lead-to-lists.md) | `POST /public/v1/leads/:lead_id/add-to-list` | [docs](https://docs.dealmachine.com/) |
| [Add Tags To Lead](actions/add-tags-to-lead.md) | `POST /public/v1/leads/:lead_id/add-tags` | [docs](https://docs.dealmachine.com/) |
| [Assign Team Member To Lead](actions/assign-team-member-to-lead.md) | `POST /public/v1/leads/:lead_id/assign-lead` | [docs](https://docs.dealmachine.com/) |
| [Create Lead Note](actions/create-lead-note.md) | `POST /public/v1/leads/:lead_id/create-note` | [docs](https://docs.dealmachine.com/) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /public/v1/leads/:lead_id` | [docs](https://docs.dealmachine.com/) |
| [End Lead Mail Sequence](actions/end-lead-mail-sequence.md) | `POST /public/v1/leads/:lead_id/end-mail-sequence` | [docs](https://docs.dealmachine.com/) |
| [Get Lead](actions/get-lead.md) | `GET /public/v1/leads/:lead_id` | [docs](https://docs.dealmachine.com/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /public/v1/custom-fields/` | [docs](https://docs.dealmachine.com/) |
| [List Lead Statuses](actions/list-lead-statuses.md) | `GET /public/v1/lead-statuses/` | [docs](https://docs.dealmachine.com/) |
| [List Leads](actions/list-leads.md) | `GET /public/v1/leads/` | [docs](https://docs.dealmachine.com/) |
| [List Lists](actions/list-lists.md) | `GET /public/v1/lists/` | [docs](https://docs.dealmachine.com/) |
| [List Mail Sequences](actions/list-mail-sequences.md) | `GET /public/v1/mail-sequences/` | [docs](https://docs.dealmachine.com/) |
| [List Tags](actions/list-tags.md) | `GET /public/v1/tags/` | [docs](https://docs.dealmachine.com/) |
| [List Team Members](actions/list-team-members.md) | `GET /public/v1/team-members/` | [docs](https://docs.dealmachine.com/) |
| [Pause Lead Mail Sequence](actions/pause-lead-mail-sequence.md) | `POST /public/v1/leads/:lead_id/pause-mail-sequence` | [docs](https://docs.dealmachine.com/) |
| [Remove Lead From Lists](actions/remove-lead-from-lists.md) | `POST /public/v1/leads/:lead_id/remove-from-list` | [docs](https://docs.dealmachine.com/) |
| [Remove Tags From Lead](actions/remove-tags-from-lead.md) | `POST /public/v1/leads/:lead_id/remove-tags` | [docs](https://docs.dealmachine.com/) |
| [Start Lead Mail Sequence](actions/start-lead-mail-sequence.md) | `POST /public/v1/leads/:lead_id/start-mail-sequence` | [docs](https://docs.dealmachine.com/) |
| [Update Lead Custom Field](actions/update-lead-custom-field.md) | `POST /public/v1/leads/:lead_id/custom-field` | [docs](https://docs.dealmachine.com/) |
| [Update Lead Status](actions/update-lead-status.md) | `POST /public/v1/leads/:lead_id/lead-status` | [docs](https://docs.dealmachine.com/) |
