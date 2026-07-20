# Reject Purchase with LeadDyno

Rejects a pending purchase in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/purchases/:id/reject`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Reject Purchase](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/reject-a-purchase-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The purchase ID. |
