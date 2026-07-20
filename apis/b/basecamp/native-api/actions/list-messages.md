# List Messages with Basecamp

Retrieves messages from a Basecamp message board.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/message_boards/:boardId/messages.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [List Messages](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#get-messages)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `boardId` | path | `number` | yes |
