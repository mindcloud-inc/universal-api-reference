# Spoki: Native API Reference

A consolidated summary of Spoki's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/21611004/UzBqnPvF
- **API base URL:** `https://api.spoki.com/api/1`

## Authentication

### API Key

Use your Spoki API key in the X-Spoki-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.spoki.com/en/docs/integrations/integrate-spoki-with-any-management-system-via-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Automation](actions/create-automation.md) | `POST /automations/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Create List](actions/create-list.md) | `POST /lists/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Create Template](actions/create-template.md) | `POST /templates/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [List Automations](actions/list-automations.md) | `GET /automations/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [List Lists](actions/list-lists.md) | `GET /lists/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [List Templates](actions/list-templates.md) | `GET /templates/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Retrieve Automation](actions/retrieve-automation.md) | `GET /automations/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Retrieve Campaign](actions/retrieve-campaign.md) | `GET /campaigns/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Retrieve List](actions/retrieve-list.md) | `GET /lists/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /templates/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Sync Contacts](actions/sync-contacts.md) | `POST /contacts/sync/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Sync List Contacts](actions/sync-list-contacts.md) | `POST /lists/{{id}}/sync_contacts/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
| [Update Template](actions/update-template.md) | `PATCH /templates/{{id}}/` | [docs](https://documenter.getpostman.com/view/21611004/UzBqnPvF) |
