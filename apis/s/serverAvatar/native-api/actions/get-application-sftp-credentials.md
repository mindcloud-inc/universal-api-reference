# Get Application SFTP Credentials with ServerAvatar

Retrieves application SFTP credentials from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/applications/{{application}}/sftp`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [Get Application SFTP Credentials](https://serveravatar.com/api-docs/endpoint/application/sftp-credentials.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
| `application` | path | `string` | yes |
