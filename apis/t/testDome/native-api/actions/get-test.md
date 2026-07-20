# Get Test with TestDome

Retrieves a test from TestDome.

## Endpoint

- **Method:** `GET`
- **Path:** `/tests/:testId`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Get Test](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `list<string>` | no |
| `$select` | query | `list<string>` | no |
| `id` | path | `number` | yes |
