# Search Quality Profiles with SonarQube

Finds quality profiles in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/qualityprofiles/search`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Quality Profiles](https://sonarcloud.io/web_api/api/qualityprofiles/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/qualityprofiles/search. |
