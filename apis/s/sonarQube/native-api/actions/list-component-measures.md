# List Component Measures with SonarQube

Retrieves component measures from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/measures/component_tree`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [List Component Measures](https://sonarcloud.io/web_api/api/measures/component_tree)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component` | query | `string` | yes | Component key. Required by /api/measures/component_tree. |
| `metricKeys` | query | `string` | yes | Comma-separated metric keys. Required by /api/measures/component_tree. |
