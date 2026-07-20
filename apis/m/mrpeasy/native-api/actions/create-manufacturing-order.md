# Create Manufacturing Order with MRPeasy

Creates a new manufacturing order in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/manufacturing-orders`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create Manufacturing Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | body | `number` | yes | MRPeasy article ID to manufacture. |
| `quantity` | body | `number` | yes | Manufacturing quantity. |
| `bom_id` | body | `number` | yes | MRPeasy BOM ID. |
| `routing_id` | body | `number` | yes | MRPeasy routing ID. |
| `assigned_id` | body | `number` | yes | MRPeasy assigned user ID. |
