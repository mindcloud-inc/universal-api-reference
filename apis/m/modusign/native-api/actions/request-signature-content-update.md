# Request Signature Content Update with Modusign

Requests a signature content correction in Modusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:documentId/request-correction`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Request Signature Content Update](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `message` | body | `string` | yes | The correction request message shown to the participant. |
| `participantId` | body | `string` | yes | The participant ID whose signature content should be corrected. |
