# Soft Delete Channel Message Reply with Microsoft Teams

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/teams/:teamId/channels/:channelId/messages/:messageId/replies/:replyId/softDelete`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Soft Delete Channel Message Reply](https://learn.microsoft.com/en-us/graph/api/chatmessage-softdelete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `channelId` | path | `string` | yes |
| `messageId` | path | `string` | yes |
| `replyId` | path | `string` | yes |
