# Cancel Signature Request with Modusign

Cancels an existing signature request in Modusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:documentId/cancel`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Cancel Signature Request](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `message` | body | `string` | yes | A 2-200 character cancellation message shown with the cancelled signature request. |
