# Create SFTP Credentials with Dromo

Creates new SFTP credentials in Dromo.

## Endpoint

- **Method:** `POST`
- **Path:** `/headless/sftp/credentials/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Create SFTP Credentials](https://developer.dromo.io/api-reference/sftp-credentials/create-sftp-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | body | `string` | yes | Request body field hostname. |
| `port` | body | `number` | yes | Request body field port. |
| `user` | body | `string` | yes | Request body field user. |
| `auth_type` | body | `string` | yes | Request body field auth_type. |
| `password` | body | `string` | no | Request body field password. |
| `private_key` | body | `string` | no | Request body field private_key. |
