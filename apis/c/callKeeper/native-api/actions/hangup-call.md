# Hangup Call with CallKeeper

Updates a call in CallKeeper by hanging up.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/:call_id/hangup`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Hangup Call](https://api.callkeeper.ai/docs#/Calls/hangup_call_calls__call_id__hangup_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `string` | yes | Call ID. |
