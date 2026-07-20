# Send API Visitor Slider Response with WotNot

Creates an API visitor slider response in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send API Visitor Slider Response](https://help.wotnot.io/deploy/publishing-agents/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | API-channel conversation ID |
| `message.data.body` | body | `string` | yes | Slider label body |
| `message.data.value` | body | `number` | yes | Numeric slider value |
| `message.data.callback` | body | `string` | no | Optional callback value |
