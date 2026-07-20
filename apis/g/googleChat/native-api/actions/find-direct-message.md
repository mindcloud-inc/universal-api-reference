# Find Direct Message with Google Chat

Finds an existing Google Chat direct message with a user.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces\:findDirectMessage`
- **Base URL:** `https://chat.googleapis.com/v1`
- **Official documentation:** [Find Direct Message](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/findDirectMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Enter the user's email address or Google Chat user ID. MindCloud will send it to Google as users/{value}. You can also paste a full users/... value. |
