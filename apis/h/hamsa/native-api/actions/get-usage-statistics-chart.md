# Get Usage Statistics Chart with Hamsa

Retrieves usage statistics chart data from Hamsa.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/statistics/chart`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Get Usage Statistics Chart](https://docs.tryhamsa.com/api-reference/endpoint/statistics-chart)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startPeriod` | query | `string` | yes |
| `endPeriod` | query | `string` | yes |
| `projectId` | query | `string` | yes |
