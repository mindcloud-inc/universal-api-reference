# List Voices with LMNT

Retrieves a list of available voices from LMNT.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/ai/voice/list`
- **Base URL:** `https://api.lmnt.com`
- **Official documentation:** [List Voices](https://docs.lmnt.com/api-reference/voice/list-voices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | query | `string` | no | Which owner's voices to return: system, me, or all. |
| `starred` | query | `boolean` | no | When true, only returns starred voices. |
