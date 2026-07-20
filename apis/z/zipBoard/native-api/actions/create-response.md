# Create Response with zipBoard

Creates a new response in zipBoard.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/responses`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Create Response](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attachments[]` | body | `array<string>` | no |
| `mentionedIds` | body | `string<string>` | no |
| `reply` | body | `string` | yes |
| `reply_id` | body | `string` | no |
| `route` | body | `string` | yes |
| `taskid` | body | `string` | yes |
| `user_id` | body | `string` | no |
