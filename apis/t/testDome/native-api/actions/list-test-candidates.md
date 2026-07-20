# List Test Candidates with TestDome

Retrieves test candidates from TestDome.

## Endpoint

- **Method:** `GET`
- **Path:** `/tests/:testId/candidates`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [List Test Candidates](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `list<string>` | no |
| `$filter[archived]` | query | `boolean` | no |
| `$filter[notified]` | query | `boolean` | no |
| `$filter[status]` | query | `string` | no |
| `$filter[term]` | query | `string` | no |
| `$select` | query | `list<string>` | no |
| `$sort` | query | `list<string>` | no |
| `id` | path | `number` | yes |
