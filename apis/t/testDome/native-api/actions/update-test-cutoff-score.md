# Update Test Cutoff Score with TestDome

Updates a test cutoff score in TestDome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tests/:testId/cutoff-score`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Update Test Cutoff Score](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cutoffScore` | body | `number` | yes |
| `id` | path | `number` | yes |
