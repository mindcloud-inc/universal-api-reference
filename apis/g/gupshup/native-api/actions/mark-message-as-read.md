# Mark Message As Read with Gupshup

Marks a message as read in Gupshup.

## Endpoint

- **Method:** `PUT`
- **Path:** `/wa/app/{appId}/msg/{msgId}/read`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Mark Message As Read](https://docs.gupshup.io/reference/mark-message-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Gupshup app ID. |
| `msgId` | path | `string` | yes | Gupshup message ID to mark as read. |
