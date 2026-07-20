# Search Measure History with SonarQube

Finds measure history in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/measures/search_history`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Measure History](https://sonarcloud.io/web_api/api/measures/search_history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component` | query | `string` | yes | Component key. Required by /api/measures/search_history. |
| `component` | query | `string` | yes | Component key. Required by /api/measures/search_history. |
| `metrics` | query | `string` | yes | Comma-separated metric keys. Required by /api/measures/search_history. |
