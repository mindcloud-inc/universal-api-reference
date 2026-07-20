# Update SFTP Credentials with Dromo

Updates existing SFTP credentials in Dromo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/headless/sftp/credentials/:id/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Update SFTP Credentials](https://developer.dromo.io/api-reference/sftp-credentials/update-sftp-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
| `hostname` | body | `string` | yes | Request body field hostname. |
| `port` | body | `number` | yes | Request body field port. |
| `user` | body | `string` | yes | Request body field user. |
| `auth_type` | body | `string` | yes | Request body field auth_type. |
| `password` | body | `string` | no | Request body field password. |
| `private_key` | body | `string` | no | Request body field private_key. |
