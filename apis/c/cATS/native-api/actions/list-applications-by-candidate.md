# List Applications By Candidate with CATS

Retrieves applications for a candidate in CATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/:candidate_id/applications`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [List Applications By Candidate](https://docs.catsone.com/api/v3/#candidates-list-applications-by-candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | path | `number` | yes | The ID of the candidate to return applications for. |
