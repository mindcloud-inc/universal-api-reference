# Cancel Pickup with EasyPost

Cancels an existing pickup in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/pickups/:id/cancel`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Cancel Pickup](https://docs.easypost.com/docs/pickups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Pickup ID, beginning with pickup_. |
