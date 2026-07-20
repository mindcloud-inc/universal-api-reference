# Cancel Pickup with Easyship

Cancels a pickup in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/pickups/:pickup_id/cancel`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Cancel Pickup](https://developers.easyship.com/reference/pickups_cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pickup_id` | path | `string` | yes | The Easyship pickup ID. |
