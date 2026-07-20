# Unarchive Stream with Faraday

Unarchives an existing stream in Faraday.

## Endpoint

- **Method:** `POST`
- **Path:** `/streams/:stream_id_or_name/unarchive`
- **Base URL:** `https://api.faraday.ai/v1`
- **Official documentation:** [Unarchive Stream](https://faraday.ai/docs/reference/unarchivestream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id_or_name` | path | `string` | no | Faraday stream ID or name. |
