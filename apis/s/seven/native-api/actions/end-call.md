# End Call with Seven

Ends a voice call in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/:call_id/hangup`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [End Call](https://docs.seven.io/en/rest-api/endpoints/voice#end-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `string` | yes | The ID of the call to be ended. |
