# Update a Field with Quickbase

Updates an existing field in Quickbase.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/fields/:fieldId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Update a Field](https://developer.quickbase.com/operation/updateField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `fieldId` | path | `number` | yes | The Quickbase field identifier. |
| `label` | body | `string` | no | Optional new field label. |
| `fieldHelp` | body | `string` | no | Optional new help text for the field. |
