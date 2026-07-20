# Archive Candidates with TestDome

Archives candidates in TestDome.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates/archive`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Archive Candidates](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `candidateIds` | body | `list<number>` | yes |
