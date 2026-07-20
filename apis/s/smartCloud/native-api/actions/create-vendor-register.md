# Register vendor with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/register`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Register vendor](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | body | `string` | yes | User email |
| `password` | body | `string` | yes | Password (should contain at least 1 number, 1 capital and 1 lowercase letter and be 8 more characters long) |
| `password_retype` | body | `string` | yes | Repeated password |
| `invite_code` | body | `string` | yes | Invite code to register in platform |
