# Restore Big Data Operations with SeaTable

Restores big data operations in a SeaTable base.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/restore-operations/:op_id/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Restore Big Data Operations](https://api.seatable.com/reference/restorebigdataoperations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `op_id` | path | `string` | yes | The SeaTable operation ID. |
