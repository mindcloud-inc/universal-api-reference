# List Quality Profile Projects with SonarQube

Retrieves projects for a quality profile in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/qualityprofiles/projects`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Quality Profile Projects](https://sonarcloud.io/web_api/api/qualityprofiles/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | yes | Quality profile key. Required by /api/qualityprofiles/projects. |
