# Get Candidate with TestDome

Retrieves a candidate from TestDome.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/:candidateId`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Get Candidate](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `list<string>` | no |
| `$select` | query | `list<string>` | no |
| `candidateId` | path | `number` | yes |
