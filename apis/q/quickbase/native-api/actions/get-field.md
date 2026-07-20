# Get Field with Quickbase

Retrieves a Quickbase field by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/fields/:fieldId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Get Field](https://developer.quickbase.com/operation/getField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `fieldId` | path | `number` | yes | The Quickbase field identifier. |
| `includeFieldPerms` | query | `boolean` | no | Whether to include field permission details in the response. |
