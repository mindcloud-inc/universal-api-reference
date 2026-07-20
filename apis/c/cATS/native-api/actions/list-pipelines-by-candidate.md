# List Pipelines By Candidate with CATS

Retrieves pipelines for a candidate in CATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/:id/pipelines`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [List Pipelines By Candidate](https://docs.catsone.com/api/v3/#candidates-list-pipelines-by-candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the candidate to return pipelines for. |
