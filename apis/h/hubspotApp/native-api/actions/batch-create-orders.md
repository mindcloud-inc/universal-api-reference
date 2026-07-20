# Batch Create Orders with HubSpot

Creates new orders in HubSpot in a batch.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/orders/batch/create`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Batch Create Orders](https://developers.hubspot.com/docs/api-reference/crm-orders-v3/batch/post-crm-v3-objects-orders-batch-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | Array of order objects to create (HubSpot batch create payload). |
