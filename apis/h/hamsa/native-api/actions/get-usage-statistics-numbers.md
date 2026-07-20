# Get Usage Statistics Numbers with Hamsa

Retrieves usage statistic totals from Hamsa.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/statistics/numbers`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Get Usage Statistics Numbers](https://docs.tryhamsa.com/api-reference/endpoint/statistics-numbers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `startPeriod` | query | `string` | yes |
| `endPeriod` | query | `string` | yes |
| `projectId` | query | `string` | yes |
