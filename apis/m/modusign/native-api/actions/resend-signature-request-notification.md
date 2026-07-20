# Resend Signature Request Notification with Modusign

Resends a signing notification in Modusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:documentId/remind-signing`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Resend Signature Request Notification](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
