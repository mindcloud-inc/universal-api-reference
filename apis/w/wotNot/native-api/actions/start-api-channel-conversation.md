# Start API Channel Conversation with WotNot

Creates an API channel conversation in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversations`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Start API Channel Conversation](https://help.wotnot.io/deploy/publishing-agents/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.data.body` | body | `string` | yes | Initial visitor message |
| `publish_key` | body | `string` | yes | API-channel publish key from the API bot |
| `from.user_external_id` | body | `string` | yes | Unique visitor ID from your system |
