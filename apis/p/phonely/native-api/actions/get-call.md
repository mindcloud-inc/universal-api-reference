# Get Call with Phonely

Retrieves a call from Phonely.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-call`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Get Call](https://docs.phonely.ai/api-reference/endpoint/get-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | The Phonely user ID that owns the target call. |
| `agentId` | body | `string` | yes | The Phonely agent ID that received the call. |
| `callId` | body | `string` | yes | The Phonely call ID to retrieve. |
