# Get Call Transcript with Dialpad

Retrieves a Dialpad AI transcript for a call.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcripts/:call_id`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Get Call Transcript](https://developers.dialpad.com/reference/transcriptsget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_id` | path | `number` | yes | The call's id. |
