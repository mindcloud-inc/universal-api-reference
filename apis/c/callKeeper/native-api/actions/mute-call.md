# Mute Call with CallKeeper

Updates a call in CallKeeper by muting it.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/:call_id/mute`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Mute Call](https://api.callkeeper.ai/docs#/Calls/mute_call_calls__call_id__mute_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `string` | yes | Call ID. |
