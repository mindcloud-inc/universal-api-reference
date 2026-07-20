# Send Message with Orimon

Creates a chatbot message in Orimon.

## Endpoint

- **Method:** `POST`
- **Path:** `/orimon/v1/conversation/api/message`
- **Base URL:** `https://channel-connector.orimon.ai`
- **Official documentation:** [Send Message](https://orimon.gitbook.io/docs/developer-api/message-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `info.tenantId` | body | `string` | yes | The unique ID of the chatbot you want to message. |
| `info.psid` | body | `string` | yes | A unique session identifier for the end user; docs recommend a random value plus '_' plus the tenantId. |
| `message.payload.text` | body | `string` | yes | The user message to send to the chatbot. |
| `message.id` | body | `string` | yes | A unique identifier for this input message. |
