# Create Driver with Zeo Route Planner

Creates a new driver in Zeo Route Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v5/drivers`
- **Base URL:** `https://zeorouteplanner.com`
- **Official documentation:** [Create Driver](https://api.zeorouteplanner.com/create-drivers.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Driver address. |
| `email` | body | `string` | no | Driver email. |
| `name` | body | `string` | no | Name of the driver. |
| `password` | body | `string` | no | Password for the driver account. |
| `phone_no` | body | `string` | no | Driver phone number. |
