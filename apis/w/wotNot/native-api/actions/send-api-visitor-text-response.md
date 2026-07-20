# Send API Visitor Text Response with WotNot

Creates an API visitor text response in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send API Visitor Text Response](https://help.wotnot.io/deploy/publishing-agents/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | API-channel conversation ID |
| `message.data.body` | body | `string` | yes | Visitor message text |
