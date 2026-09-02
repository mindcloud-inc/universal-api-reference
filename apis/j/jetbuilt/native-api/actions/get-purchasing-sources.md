# Get Purchasing Sources with Jetbuilt

## Endpoint

- **Method:** `GET`
- **Path:** `purchasing/sources/:iD`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get Purchasing Sources](https://api.jetbuilt.com/customers#get-a-purchase-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `min_updated_at` | query | `string` | no | — |
| `project_id` | query | `string` | no | — |
| `min_created_at` | query | `string` | no | — |
| `iD` | path | `string` | no | The ID of the purchasing source to retrieve |
