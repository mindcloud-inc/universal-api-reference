# Plasmic: Native API Reference

A consolidated summary of Plasmic's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.plasmic.app/learn/plasmic-cms-api-reference/
- **API base URL:** `https://data.plasmic.app/api/v1/cms`

## Authentication

### Plasmic CMS Tokens

Store the Plasmic CMS ID plus public and secret tokens. Read actions use the public token; write actions use the secret token.

### Credentials

- **CMS ID:** `cmsId` · required · The CMS ID from your Plasmic CMS Settings page.
- **Public Token:** `publicToken` · required · The public token used for read operations.
- **Secret Token:** `secretToken` · required · The secret token used for create, update, delete, and draft-read operations.

[Official authentication documentation](https://docs.plasmic.app/learn/plasmic-cms-api-reference/)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Draft Items](actions/count-draft-items.md) | `GET /databases/{{credentials.cmsId}}/tables/:modelId/count` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Count Items](actions/count-items.md) | `GET /databases/{{credentials.cmsId}}/tables/:modelId/count` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Create Items](actions/create-items.md) | `POST /databases/{{credentials.cmsId}}/tables/:modelId/rows` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Delete Item](actions/delete-item.md) | `DELETE /rows/:rowId` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Publish Item](actions/publish-item.md) | `POST /rows/:rowId/publish` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Query Draft Items](actions/query-draft-items.md) | `GET /databases/{{credentials.cmsId}}/tables/:modelId/query` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Query Items](actions/query-items.md) | `GET /databases/{{credentials.cmsId}}/tables/:modelId/query` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
| [Update Item](actions/update-item.md) | `PUT /rows/:rowId` | [docs](https://docs.plasmic.app/learn/plasmic-cms-api-reference/) |
