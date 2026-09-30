# Patch Custom Table Field with Microsoft Dynamics 365

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:tableName(:id)`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields[]` | body | `array` | no |
| `customFields[].customKey` | body | `string` | no |
| `customFields[].customValue` | body | `string` | no |
| `id` | path | `string` | no |
| `tableName` | path | `string` | no |
