# List Project Lists with KiteSuite

Retrieves a list from KiteSuite by list ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/list/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [List Project Lists](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | This endpoint returned a single list when called with a list ID at runtime, despite the Swagger summary implying a project ID. |
