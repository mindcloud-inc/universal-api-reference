# Create Poll with Stream

Creates a new poll in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/polls`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Create Poll](https://getstream.io/chat/docs/javascript/polls_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Poll name. |
| `options[]` | body | `array<object>` | no | Poll options array. |
| `user_id` | body | `string` | no | User ID creating the poll. |
