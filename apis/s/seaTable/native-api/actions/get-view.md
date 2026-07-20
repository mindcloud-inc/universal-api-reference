# Get View with SeaTable

Retrieves a view from a SeaTable base.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/views/:view_name/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Get View](https://api.seatable.com/reference/getview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_name` | path | `string` | yes | The SeaTable view name. |
