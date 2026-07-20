# List User Groups For User with SonarQube

Retrieves user groups for a SonarQube user.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/users/groups`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List User Groups For User](https://sonarcloud.io/web_api/api/users/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | query | `string` | yes | User login. Required by /api/users/groups. |
| `organization` | query | `string` | yes | Organization key. Required by /api/users/groups. |
