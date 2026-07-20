# Notify Test Candidates with TestDome

Notifies test candidates in TestDome.

## Endpoint

- **Method:** `POST`
- **Path:** `/tests/:testId/candidates/notify`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Notify Test Candidates](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `candidateIds` | body | `list<number>` | yes |
| `failEmail` | body | `string` | no |
| `id` | path | `number` | yes |
| `passEmail` | body | `string` | no |
| `replyTo` | body | `string` | yes |
