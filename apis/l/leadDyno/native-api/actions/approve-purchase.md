# Approve Purchase with LeadDyno

Approves a pending purchase in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/purchases/:id/approve`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Approve Purchase](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/approve-a-purchase-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The purchase ID. |
