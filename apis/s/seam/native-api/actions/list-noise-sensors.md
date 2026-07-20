# List Noise Sensors with Seam

Retrieves a list of noise sensors from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/noise_sensors/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Noise Sensors](https://docs.seam.co/latest/api/noise_sensors/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connected_account_id` | body | `string` | no | ID of the connected account for which you want to list noise sensors. |
| `search` | body | `string` | no | Search string for noise sensors. |
| `space_id` | body | `string` | no | ID of the space for which you want to list noise sensors. |
