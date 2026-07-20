# Get Pickup with EasyPost

Retrieves details for a pickup from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/pickups/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Pickup](https://docs.easypost.com/docs/pickups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Pickup ID, beginning with pickup_. |
