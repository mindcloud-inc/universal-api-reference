# Update View with SeaTable

Updates a view in a SeaTable base.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/views/:view_name/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Update View](https://api.seatable.com/reference/updateview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_name` | path | `string` | yes | The SeaTable view name. |
