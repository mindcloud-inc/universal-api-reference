# Get Candidate Application with CATS

Retrieves a candidate application from CATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates/applications/:application_id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Get Candidate Application](https://docs.catsone.com/api/v3/#candidates-get-a-candidate-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application_id` | path | `number` | yes | The ID of the candidate application to return. |
