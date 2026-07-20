# Get Message Board with Basecamp

Retrieves a message board from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/message_boards/:boardId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Message Board](https://github.com/basecamp/bc3-api/blob/master/sections/message_boards.md#get-message-board)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `boardId` | path | `number` | yes |
