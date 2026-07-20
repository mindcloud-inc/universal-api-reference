# Redact Conversation with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/redact`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Redact Conversation](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/redactconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Entity type to redact |
| `conversation_id` | body | `string` | yes | Conversation identifier for redaction |
| `source` | body | `string` | yes | Reason/source for redaction |
| `source_id` | body | `string` | no | Required when redacting type=source |
| `conversation_part_id` | body | `string` | no | Required when redacting type=conversation_part |
