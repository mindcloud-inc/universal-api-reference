# Search Projects with SonarQube

Finds projects in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/projects/search`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Projects](https://sonarcloud.io/web_api/api/projects/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/projects/search. |
