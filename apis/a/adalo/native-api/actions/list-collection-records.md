# List Collection Records with Adalo

Retrieves records from a specific Adalo collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/apps/:appId/collections/:collectionId`
- **Base URL:** `https://api.adalo.com`
- **Official documentation:** [List Collection Records](https://help.adalo.com/integrations/the-adalo-api/collections)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The Adalo app ID that owns the collection. |
| `collectionId` | path | `string` | yes | The collection ID to read records from. |
| `filterKey` | query | `string` | no | Optional single-value collection field to filter by. Use Number, Text, Boolean, or Date properties only. |
| `filterValue` | query | `string` | no | Optional value for the filter field. Must match the selected single-value property format. |
