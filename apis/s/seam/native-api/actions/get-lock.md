# Get Lock with Seam

Retrieves a lock from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/locks/get`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Get Lock](https://docs.seam.co/latest/api/locks/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | body | `string` | no | ID of the lock that you want to get. |
| `name` | body | `string` | no | Name of the lock that you want to get. |
