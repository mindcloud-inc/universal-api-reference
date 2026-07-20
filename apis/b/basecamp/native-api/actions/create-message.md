# Create Message with Basecamp

Creates a new message on a Basecamp message board.

## Endpoint

- **Method:** `POST`
- **Path:** `/:accountId/message_boards/:boardId/messages.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Create Message](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#create-a-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `boardId` | path | `number` | yes |
| `subject` | body | `string` | yes |
| `content` | body | `string` | no |
| `category_id` | body | `number` | no |
| `subscriptions[]` | body | `array<number>` | no |
