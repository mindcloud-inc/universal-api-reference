# Get Record with Airtable

Retrieves a specific record from an Airtable table.

## Endpoint

- **Method:** `GET`
- **Path:** `/:baseId/:tableId/:recordId`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [Get Record](https://airtable.com/developers/web/api/get-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes | To get this value, check this doc https://airtable.com/developers/web/api/list-bases |
| `tableId` | path | `list<string>` | yes | — |
| `recordId` | path | `string` | yes | The ID of the Airtable Record to retrieve. |
