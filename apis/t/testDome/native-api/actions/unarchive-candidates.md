# Unarchive Candidates with TestDome

Unarchives candidates in TestDome.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates/unarchive`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Unarchive Candidates](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `candidateIds` | body | `list<number>` | yes |
