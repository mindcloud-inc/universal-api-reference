# Update Test URL with TestDome

Updates an existing test URL in TestDome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tests/:testId/urls/:testUrlId`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Update Test URL](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `disabled` | body | `boolean` | no |
| `id` | path | `number` | yes |
| `testUrlId` | path | `number` | yes |
