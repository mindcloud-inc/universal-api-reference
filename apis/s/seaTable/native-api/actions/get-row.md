# Get Row with SeaTable

Retrieves a row from a SeaTable base.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/rows/:row_id/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Get Row](https://api.seatable.com/reference/getrow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `row_id` | path | `string` | yes | The SeaTable row ID. |
