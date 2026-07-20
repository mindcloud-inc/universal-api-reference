# Hangup/reject an active call with Routee

Hangs up or rejects an active call in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/voice/conversation/:messageId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Hangup/reject an active call](https://docs.routee.net/reference/hangupreject-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call |
| `action` | body | `string` | yes | Defines the action to perform. Values: "hangup", "reject". Hangup only apply to calls with "InProgress" status. Reject only apply to calls with "Ringing" or "Initiated") |
