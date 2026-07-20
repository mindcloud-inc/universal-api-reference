# Feishu Base: Native API Reference

A consolidated summary of Feishu Base's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://open.feishu.cn/document/server-docs/docs/bitable-v1/app/get
- **API base URL:** `https://open.feishu.cn/open-apis/bitable/v1`

## Authentication

### Custom App Credentials

Use a Feishu custom app's app_id and app_secret to obtain a tenant_access_token for Bitable requests.

### Credentials

- **App ID:** `appId` · required · Feishu custom app identifier used to request tenant_access_token.
- **App Secret:** `appSecret` · required · Feishu custom app secret used to request tenant_access_token.

Send these headers with each API request:

```http
Authorization: Bearer <custom.tenantAccessToken>
```

[Official authentication documentation](https://open.feishu.cn/document/server-docs/authentication-management/access-token/tenant_access_token_internal)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | `GET /apps/:app_token` | [docs](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app/get) |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | `POST https://open.feishu.cn/open-apis/auth/v3/tenant_access_token/internal` | [docs](https://open.feishu.cn/document/server-docs/authentication-management/access-token/tenant_access_token_internal) |
| [List Fields](actions/list-fields.md) | `GET /apps/:app_token/tables/:table_id/fields` | [docs](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table-field/list) |
| [List Records](actions/list-records.md) | `GET /apps/:app_token/tables/:table_id/records` | [docs](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table-record/list) |
| [List Tables](actions/list-tables.md) | `GET /apps/:app_token/tables` | [docs](https://open.feishu.cn/document/server-docs/docs/bitable-v1/app-table/list) |
