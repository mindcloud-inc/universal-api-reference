# Search Components with SonarQube

Finds components in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/components/search`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Components](https://sonarcloud.io/web_api/api/components/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/components/search. |
