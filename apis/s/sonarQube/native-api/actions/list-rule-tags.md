# List Rule Tags with SonarQube

Retrieves rule tags from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/rules/tags`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Rule Tags](https://sonarcloud.io/web_api/api/rules/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/rules/tags. |
