# Search Project Analyses with SonarQube

Finds project analyses in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/project_analyses/search`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Project Analyses](https://sonarcloud.io/web_api/api/project_analyses/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Project key. Required by /api/project_analyses/search. |
