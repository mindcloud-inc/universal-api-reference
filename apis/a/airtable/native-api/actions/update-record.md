# Update Record with Airtable

Updates a record in a specific Airtable table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:baseId/:tableId/:recordId`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [Update Record](https://airtable.com/developers/web/api/update-record)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes |
| `tableId` | path | `list<string>` | yes |
| `recordId` | path | `string` | yes |
| `fields` | body | `object` | no |
