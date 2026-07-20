# List Issue Authors with SonarQube

Retrieves issue authors from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/issues/authors`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Issue Authors](https://sonarcloud.io/web_api/api/issues/authors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/issues/authors. |
