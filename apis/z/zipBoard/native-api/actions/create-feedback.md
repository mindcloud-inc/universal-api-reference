# Create Feedback with zipBoard

Creates a new feedback comment in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/comments`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create Feedback](https://help.zipboard.co/article/182-api-for-issues-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional feedback description. |
| `projectid` | body | `string` | yes | Project ID where the feedback should be created. |
| `projectid` | body | `string` | yes | — |
| `title` | body | `string` | yes | Feedback title. |
