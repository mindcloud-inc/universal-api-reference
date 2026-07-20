# Get Fields for a Table with Quickbase

Retrieves all fields in a Quickbase table.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/fields`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Get Fields for a Table](https://developer.quickbase.com/operation/getFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `includeFieldPerms` | query | `boolean` | no | Whether to include field permission details in the response. |
