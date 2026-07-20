# Create Test URL with TestDome

Creates a new test URL in TestDome.

## Endpoint

- **Method:** `POST`
- **Path:** `/tests/:testId/urls`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Create Test URL](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
