# Search User Groups with SonarQube

Finds user groups in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/user_groups/search`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search User Groups](https://sonarcloud.io/web_api/api/user_groups/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | Organization key. Required by /api/user_groups/search. |
