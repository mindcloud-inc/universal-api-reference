# Archive Stream with Faraday

Archives an existing stream in Faraday.

## Endpoint

- **Method:** `POST`
- **Path:** `/streams/:stream_id_or_name/archive`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Archive Stream](https://faraday.ai/docs/reference/archivestream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id_or_name` | path | `string` | no | Faraday stream ID or name. |
