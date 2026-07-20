# Get Chat History with Alltius

Retrieves chat history for an Alltius session.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/history`
- **Base URL:** `https://app.alltius.ai/api/platform`
- **Official documentation:** [Get Chat History](https://app.alltius.ai/api/platform/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | body | `string` | yes | — |
| `cursor` | body | `string` | no | — |
| `page_size` | body | `number` | no | Number of messages to fetch. |
