# Get Device with Seam

Retrieves a device from Seam by ID or name.

## Endpoint

- **Method:** `POST`
- **Path:** `/devices/get`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Get Device](https://docs.seam.co/latest/api/devices/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | body | `string` | no | ID of the device that you want to get. |
| `name` | body | `string` | no | Name of the device that you want to get. |
