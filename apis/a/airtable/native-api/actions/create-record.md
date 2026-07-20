# Create Record with Airtable

Creates a new record in a specific Airtable table.

## Endpoint

- **Method:** `POST`
- **Path:** `/:baseId/:tableId`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [Create Record](https://airtable.com/developers/web/api/create-records)

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
| `body` | body | `object` | no |
