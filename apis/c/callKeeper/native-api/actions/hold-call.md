# Hold Call with CallKeeper

Updates a call in CallKeeper by placing it on hold.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/:call_id/hold`
- **Base URL:** `https://api.callkeeper.ai`
- **Official documentation:** [Hold Call](https://api.callkeeper.ai/docs#/Calls/hold_call_calls__call_id__hold_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `string` | yes | Call ID. |
