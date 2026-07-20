# List Component Tree with SonarQube

Retrieves a component tree from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/components/tree`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Component Tree](https://sonarcloud.io/web_api/api/components/tree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component` | query | `string` | yes | Base component key. Required by /api/components/tree. |
