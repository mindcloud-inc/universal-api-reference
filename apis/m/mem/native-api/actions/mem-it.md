# Mem It with Mem

Creates a note in Mem from raw input.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/mem-it`
- **Base URL:** `https://api.mem.ai`
- **Official documentation:** [Mem It](https://docs.mem.ai/api-reference/mem-it/mem-it)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The raw content to remember. |
| `instructions` | body | `string` | no | Optional instructions for how Mem should process the input. |
| `context` | body | `string` | no | Optional context to help Mem interpret the input. |
| `timestamp` | body | `date` | no | Optional timestamp for the captured memory. |
