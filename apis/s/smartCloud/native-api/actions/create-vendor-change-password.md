# Update vendor with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/change-password`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update vendor](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `old_password` | body | `string` | no | Previous password |
| `password` | body | `string` | no | Password (should contain at least 1 number, 1 capital and 1 lowercase letter and be 8 more characters long) |
| `password_retype` | body | `string` | no | Repeated password |
