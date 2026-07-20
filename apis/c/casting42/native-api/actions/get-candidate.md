# Get Candidate with Casting42

Retrieves a candidate from Casting42 by candidate tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/candidates/{{candidateTag}}`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Get Candidate](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidateTag` | path | `string` | yes | Unique candidate tag to fetch. |
