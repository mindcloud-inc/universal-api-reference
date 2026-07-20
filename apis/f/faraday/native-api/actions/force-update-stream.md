# Force Update Stream with Faraday

Triggers a rerun for a stream in Faraday.

## Endpoint

- **Method:** `POST`
- **Path:** `/streams/:stream_id_or_name/force_update`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Force Update Stream](https://faraday.ai/docs/reference/forceupdatestream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id_or_name` | path | `string` | no | Faraday stream ID or name. |
