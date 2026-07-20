# List Candidate Assessments with Testlify

Retrieves assessments associated with a specific Testlify candidate.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assessment/:candidateId/assessments`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [List Candidate Assessments](https://docs.testlify.com/reference/get_candidate_assessments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidateId` | path | `string` | yes | Candidate identifier. |
