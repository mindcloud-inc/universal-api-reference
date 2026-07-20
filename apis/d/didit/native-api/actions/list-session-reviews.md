# List Session Reviews with Didit

Retrieves reviews for a session from Didit.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/{sessionId}/reviews/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [List Session Reviews](https://docs.didit.me/management-api/sessions/list-reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Didit session identifier. |
