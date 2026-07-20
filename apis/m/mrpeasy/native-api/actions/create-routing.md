# Create Routing with MRPeasy

Creates a new routing in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/routings`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create Routing](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | body | `number` | yes | MRPeasy product ID for the routing. |
| `title` | body | `string` | yes | Routing title. |
| `operations` | body | `array<object>` | yes | Array of routing operations, for example [{"type_id":1,"ord":"1","description":"Op","fixed_time":1,"variable_time":1,"variable_quantity":1,"time_payment":true}]. |
