# Reset vendor password with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/reset-password`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Reset vendor password](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | no | Reset password token |
| `password` | body | `string` | no | Password (should be at leaset 6 characters long) |
| `password_retype` | body | `string` | no | Repeated password |
