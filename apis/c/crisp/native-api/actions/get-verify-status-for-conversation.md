# Get Verify Status For Conversation with Crisp

Retrieves a conversation's verify status from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/verify`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get Verify Status For Conversation](https://docs.crisp.chat/references/rest-api/v1/#get-verify-status-for-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
