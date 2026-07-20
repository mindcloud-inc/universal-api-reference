# Change user password with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/users/change-password`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Change user password](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `oldPassword` | body | `string` | no |
| `newPassword` | body | `string` | no |
