# Generate Session PDF with Didit

Retrieves a session PDF report from Didit.

## Endpoint

- **Method:** `GET`
- **Path:** `https://verification.didit.me/v3/session/{sessionId}/generate-pdf`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Generate Session PDF](https://docs.didit.me/sessions-api/generate-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Didit session identifier. |
