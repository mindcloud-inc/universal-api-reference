# Get Participant Security Link with Modusign

Retrieves a participant security link from Modusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/participants/:participantId/security-link`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Get Participant Security Link](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `participantId` | path | `string` | yes | The Modusign participant ID. |
