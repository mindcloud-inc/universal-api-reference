# Get Chat Sessions By User with Alltius

Retrieves chat sessions for an Alltius user.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/chat_session_by_uid`
- **Base URL:** `https://app.alltius.ai/api/platform`
- **Official documentation:** [Get Chat Sessions By User](https://app.alltius.ai/api/platform/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | — |
| `cursor` | body | `string` | no | — |
| `page_size` | body | `number` | no | Number of sessions to fetch. |
