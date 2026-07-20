# List Tests with TestDome

Retrieves tests from TestDome.

## Endpoint

- **Method:** `GET`
- **Path:** `/tests`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [List Tests](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `list<string>` | no |
| `$filter[archived]` | query | `string` | no |
| `$filter[excludeDeleted]` | query | `boolean` | no |
| `$filter[hasQuestions]` | query | `boolean` | no |
| `$filter[isPublished]` | query | `boolean` | no |
| `$filter[notContainsQuestions]` | query | `list<number>` | no |
| `$filter[term]` | query | `string` | no |
| `$select` | query | `list<string>` | no |
| `$sort` | query | `list<string>` | no |
