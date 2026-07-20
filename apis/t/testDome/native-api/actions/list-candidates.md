# List Candidates with TestDome

Retrieves candidates from TestDome.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [List Candidates](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `list<string>` | no |
| `$filter[archived]` | query | `boolean` | no |
| `$filter[maxScore]` | query | `number` | no |
| `$filter[minScore]` | query | `number` | no |
| `$filter[status]` | query | `list<string>` | no |
| `$filter[term]` | query | `string` | no |
| `$filter[tests]` | query | `list<number>` | no |
| `$select` | query | `list<string>` | no |
| `$sort` | query | `list<string>` | no |
