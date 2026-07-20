# Buy Pickup with EasyPost

Purchases an existing pickup in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/pickups/:id/buy`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Buy Pickup](https://docs.easypost.com/docs/pickups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier` | body | `string` | yes | Carrier to use when buying the pickup. |
| `id` | path | `string` | yes | EasyPost Pickup ID, beginning with pickup_. |
| `service` | body | `string` | yes | Carrier service to use when buying the pickup. |
