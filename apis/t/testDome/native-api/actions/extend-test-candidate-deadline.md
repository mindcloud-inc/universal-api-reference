# Extend Test Candidate Deadline with TestDome

Extends test candidate deadlines in TestDome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tests/:testId/candidates/deadline`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Extend Test Candidate Deadline](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `candidateIds` | body | `list<number>` | no |
| `id` | path | `number` | yes |
| `newDeadline` | body | `string` | no |
