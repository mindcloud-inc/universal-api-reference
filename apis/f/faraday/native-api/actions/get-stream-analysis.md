# Get Stream Analysis with Faraday

Retrieves stream event counts from Faraday.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams/:stream_id_or_name/analysis`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Get Stream Analysis](https://faraday.ai/docs/reference/getstreamanalysis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id_or_name` | path | `string` | no | Faraday stream ID or name. |
