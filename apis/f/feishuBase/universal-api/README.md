# <img src="https://images.mindcloud.co/apps/icons/feishu-document-1776187446252_1776193506663.png" alt="Feishu Base logo" width="28" height="28"> Feishu Base: Universal API

Access Feishu Base (Bitable) apps, tables, records, views, and fields through the Feishu Open Platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/feishuBase/latest
- **Category:** IT Operations / Database
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.feishu.cn
- **Vendor API docs:** https://open.feishu.cn/document/server-docs/docs/bitable-v1/app/get

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Info](actions/get-app-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuBase/latest/actions/get-app-info?connectionId=$CONNECTION_ID&appToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | GET | Retrieves a Feishu tenant access token. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from a Feishu Base table. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Feishu Base table. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | GET | Retrieves metadata for a Feishu Base app. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from a Feishu Base app. |

