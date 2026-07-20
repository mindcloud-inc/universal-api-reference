# Create a Field with Quickbase

Creates a new field in Quickbase.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/fields`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Create a Field](https://developer.quickbase.com/operation/createField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `string` | yes | The Quickbase table identifier. |
| `label` | body | `string` | yes | The field label. |
| `fieldType` | body | `string` | yes | The Quickbase field type to create. |
| `fieldHelp` | body | `string` | no | Optional help text for the field. |
