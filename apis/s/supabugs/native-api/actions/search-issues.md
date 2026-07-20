# Search Issues with Supabugs

Finds issues in Supabugs by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/search`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [Search Issues](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | Free-text issue search query. |
| `page` | body | `number` | no | Page number to request. |
| `limit` | body | `number` | no | Maximum number of issues to return. |
| `sort` | body | `string` | no | Provider sort expression. |
| `isFinal` | body | `boolean` | no | Restrict to final-status issues when true. |
| `createdById` | body | `string` | no | Filter by creator user id. |
