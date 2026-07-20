# Retrieve Conversation dial Tracking with Routee

Retrieves conversation dial tracking from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/tracking/conversation/:conversationTrackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve Conversation dial Tracking](https://docs.routee.net/reference/retrieve-conversation-dial-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationTrackingId` | path | `string` | yes | The tracking id of the conversation which includes the dials. |
