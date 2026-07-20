# Tabidoo: Native API Reference

A consolidated summary of Tabidoo's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://tabidoo.docs.apiary.io/
- **API base URL:** `https://app.tabidoo.cloud/api/v2`

## Authentication

### API Key

Use a Tabidoo Bearer API token generated in User Settings > API. A short API token is only needed for upload actions.

### Credentials

- **API Key:** `apiKey` · required
- **Short API Token:** `shortApiToken` · optional · Optional short-lived Tabidoo token used by file or image related operations such as uploads.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tabidoo.docs.apiary.io/)

## API conventions

Response data is read from `data`.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Development App From Production App](actions/create-development-app-from-production-app.md) | `POST /templates/createDevAppFromProdApp` | [docs](https://help.tabidoo.cloud/en/article/creating-a-development-app-from-a-production-app) |
| [Get App](actions/get-app.md) | `GET /apps/:appId` | [docs](https://tabidoo.docs.apiary.io/) |
| [Get Template](actions/get-template.md) | `GET /templates/:templateId` | [docs](https://tabidoo.docs.apiary.io/) |
| [List App Tables](actions/list-app-tables.md) | `GET /apps/:appId/tables` | [docs](https://tabidoo.docs.apiary.io/) |
| [List Apps](actions/list-apps.md) | `GET /apps` | [docs](https://tabidoo.docs.apiary.io/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://tabidoo.docs.apiary.io/) |
