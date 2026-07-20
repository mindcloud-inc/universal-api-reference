# List Records with Airtable

Retrieves records from a specific Airtable table.

## Endpoint

- **Method:** `GET`
- **Path:** `/:baseId/:tableId`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [List Records](https://airtable.com/developers/web/api/list-records)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes | To get this value, check this doc https://airtable.com/developers/web/api/list-bases |
| `filterByFormula` | query | `string` | no | — |
| `tableId` | path | `list<string>` | yes | — |
| `sort[0][field]` | query | `string` | no | Enter a Field name to sort by. |
| `sort[0][direction]` | query | `list<string>` | no | — |
