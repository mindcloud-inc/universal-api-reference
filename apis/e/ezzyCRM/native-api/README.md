# EzzyCRM: Native API Reference

A consolidated summary of EzzyCRM's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://ezzycrm.com/api/GetApiDocument.aspx
- **API base URL:** `https://ezzycrm.com`

## Authentication

### API Key

Connect using your EzzyCRM API key and API password.

### Credentials

- **API Key:** `apiKey` · required
- **API Password:** `apiPassword` · required · API password for your EzzyCRM account.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ezzycrm.com/api/GetApiDocument.aspx)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | `POST /api/savelead` | [docs](https://ezzycrm.com/api/PostApiDocument.aspx#savelead) |
| [List Leads](actions/list-leads.md) | `GET /api/getallleads` | [docs](https://ezzycrm.com/api/GetApiDocument.aspx#getleads) |
| [List Lost Reasons](actions/list-lost-reasons.md) | `GET /api/getalllostreasons` | [docs](https://ezzycrm.com/api/GetApiDocument.aspx#getlostreasons) |
| [List Pipelines](actions/list-pipelines.md) | `GET /api/getallpipelines` | [docs](https://ezzycrm.com/api/GetApiDocument.aspx#getpipelines) |
| [List Stages](actions/list-stages.md) | `GET /api/getallstages` | [docs](https://ezzycrm.com/api/GetApiDocument.aspx#getstages) |
| [List Users](actions/list-users.md) | `GET /api/getallusers` | [docs](https://ezzycrm.com/api/GetApiDocument.aspx#getusers) |
| [Update Lead Assignee](actions/update-lead-assignee.md) | `POST /api/assignlead` | [docs](https://ezzycrm.com/api/PostApiDocument.aspx#assignlead) |
| [Update Lead Stage](actions/update-lead-stage.md) | `POST /api/updateleadstage` | [docs](https://ezzycrm.com/api/PostApiDocument.aspx#updateleadstage) |
| [Update Lead Status](actions/update-lead-status.md) | `POST /api/updateleadstatus` | [docs](https://ezzycrm.com/api/PostApiDocument.aspx#updateleadstatus) |
