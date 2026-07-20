# Adrapid: Native API Reference

A consolidated summary of Adrapid's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.adrapid.com/api/overview
- **OpenAPI specification:** https://api.adrapid.com/spec/v1/client-api.yaml
- **API base URL:** `https://api.adrapid.com/v1/api`

## Authentication

### Bearer API Token

Use the Adrapid account API token as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.adrapid.com/api/overview)

## Pagination

Use `limit` in the query string to set the page size (default 10; minimum 10). Use `offset` in the query string as the record offset.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://docs.adrapid.com/editor/library/groups) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Create User Banner](actions/create-user-banner.md) | `POST /users/:userId/banners` | [docs](https://docs.adrapid.com/api/overview) |
| [Create User Template](actions/create-user-template.md) | `POST /users/:userId/templates` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userId` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Delete User Banner](actions/delete-user-banner.md) | `DELETE /users/:userId/banners` | [docs](https://docs.adrapid.com/api/overview) |
| [Delete User Image](actions/delete-user-image.md) | `DELETE /users/:userId/images/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Delete User Template](actions/delete-user-template.md) | `DELETE /users/:userId/templates/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Generate User SSO Token](actions/generate-user-sso-token.md) | `GET /users/:userId/sso` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get API Info](actions/get-api-info.md) | `GET /` | [docs](https://docs.adrapid.com/api/api-docs) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get User Access Token](actions/get-user-access-token.md) | `GET /users/:userId/token` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get User Access URL](actions/get-user-access-url.md) | `GET /users/:userId/access` | [docs](https://docs.adrapid.com/enterprise/whitelabel/widget) |
| [Get User Banner](actions/get-user-banner.md) | `GET /users/:userId/banners/:id` | [docs](https://docs.adrapid.com/api/overview) |
| [Get User Banner Zip](actions/get-user-banner-zip.md) | `GET /users/:userId/banners/:id/zip` | [docs](https://docs.adrapid.com/api/overview) |
| [Get User Banners Quota](actions/get-user-banners-quota.md) | `GET /users/:userId/banners/quota` | [docs](https://docs.adrapid.com/api/overview) |
| [Get User Image](actions/get-user-image.md) | `GET /users/:userId/images/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get User Images Quota](actions/get-user-images-quota.md) | `GET /users/:userId/images/quota` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get User Template](actions/get-user-template.md) | `GET /users/:userId/templates/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Get Whitelabel](actions/get-whitelabel.md) | `GET /whitelabel` | [docs](https://docs.adrapid.com/enterprise/whitelabel/administration-panel) |
| [Import User Template](actions/import-user-template.md) | `POST /users/:userId/templates/import` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.adrapid.com/editor/library/groups) |
| [List User Banners](actions/list-user-banners.md) | `GET /users/:userId/banners` | [docs](https://docs.adrapid.com/api/overview) |
| [List User Images](actions/list-user-images.md) | `GET /users/:userId/images` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [List User Templates](actions/list-user-templates.md) | `GET /users/:userId/templates` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Refresh User Access Token](actions/refresh-user-access-token.md) | `PUT /users/:userId/token` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Update User](actions/update-user.md) | `PUT /users/:userId` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Update User Template](actions/update-user-template.md) | `PUT /users/:userId/templates/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Update Whitelabel](actions/update-whitelabel.md) | `PUT /whitelabel/:id` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
| [Upload User Image](actions/upload-user-image.md) | `POST /users/:userId/images` | [docs](https://docs.adrapid.com/enterprise/administrative-api) |
