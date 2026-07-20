# Delete View with SeaTable

Deletes a view from a SeaTable base.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/views/:view_name/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Delete View](https://api.seatable.com/reference/deleteview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_name` | path | `string` | yes | The SeaTable view name. |
