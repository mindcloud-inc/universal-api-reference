# Provide Test Proctoring Consent with TestDome

Provides proctoring consent for test candidates in TestDome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tests/:testId/candidates/proctoring-consent`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Provide Test Proctoring Consent](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
