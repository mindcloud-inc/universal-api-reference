# Get Candidate Result with Testlify

Retrieves a candidate's assessment result from Testlify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assessment/:assessmentId/candidate/:candidateId`
- **Base URL:** `https://api.testlify.com`
- **Official documentation:** [Get Candidate Result](https://docs.testlify.com/reference/get_candidate_result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assessmentId` | path | `string` | yes | Assessment identifier. |
| `candidateId` | path | `string` | yes | Candidate identifier. |
| `report` | query | `string` | no | Report type. |
| `fileType` | query | `string` | no | Export file format. |
| `testLibId` | query | `string` | no | Test library identifier for report selection. |
