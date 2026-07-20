# Retrieve Conversation by TrackingId with Routee

Retrieves conversation by tracking ID from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice/conversation/:conversationTrackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve Conversation by TrackingId](https://docs.routee.net/reference/retrieve-conversation-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationTrackingId` | path | `string` | yes | The tracking id of the conversation which includes the dialPlan. |
