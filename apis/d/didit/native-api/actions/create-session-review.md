# Create Session Review with Didit

Creates a new review for a session in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/{sessionId}/reviews/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Create Session Review](https://docs.didit.me/management-api/sessions/create-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Didit session identifier. |
