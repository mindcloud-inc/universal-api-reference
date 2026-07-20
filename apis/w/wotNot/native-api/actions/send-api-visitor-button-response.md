# Send API Visitor Button Response with WotNot

Creates an API visitor button response in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send API Visitor Button Response](https://help.wotnot.io/deploy/publishing-agents/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | API-channel conversation ID |
| `message.data.body` | body | `string` | yes | Button label selected by the visitor |
| `message.data.callback` | body | `string` | yes | Callback value from the button payload |
| `message.data.next_dialog` | body | `string` | yes | Next dialog from the button payload |
| `message.data.key` | body | `string` | yes | Button key from the prior prompt payload |
