# Get Candidate with OpenFEC

Retrieves a candidate from OpenFEC.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidate/:candidate_id/`
- **Base URL:** `https://api.open.fec.gov/v1`
- **Official documentation:** [Get Candidate](https://api.open.fec.gov/developers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | path | `string` | yes | FEC candidate ID, such as P80000722. |
