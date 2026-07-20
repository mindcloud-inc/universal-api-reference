# Ask Assistant with Alltius

Submits a user query to an Alltius assistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat`
- **Base URL:** `https://app.alltius.ai/api/platform`
- **Official documentation:** [Ask Assistant](https://app.alltius.ai/api/platform/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `post` | body | `string` | yes |
| `chat_session` | body | `string` | no |
| `user_identifier` | body | `string` | no |
| `post_metadata` | body | `object` | no |
