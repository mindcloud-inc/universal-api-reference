# Patch Custom Table with Microsoft Dynamics 365

## Endpoint

- **Method:** `PATCH`
- **Path:** `:tableName(:filter)`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | — |
| `tableName` | path | `string` | yes | — |
| `filter` | path | `string` | yes | eg (ProjectID='CNY25419',dataAreaId='tci') |
