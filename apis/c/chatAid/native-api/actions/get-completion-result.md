# Get Completion Result with Chat Aid

Retrieves a Chat Aid completion result by prompt ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/completions/custom/:promptId`
- **Base URL:** `https://api.chataid.com`
- **Official documentation:** [Get Completion Result](https://docs.chataid.com/api-guide/completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `promptId` | path | `string` | yes | Unique question identifier returned by Submit Question. |
