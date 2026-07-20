# Update Funnel with Ablefy

Updates an existing funnel in Ablefy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/funnels/:id`
- **Base URL:** `https://api.myablefy.com`
- **Official documentation:** [Update Funnel](https://api.myablefy.com/api/swagger_doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Funnel ID. |
| `name` | body | `string` | no | — |
| `funnel_node_attributes` | body | `object` | yes | — |
