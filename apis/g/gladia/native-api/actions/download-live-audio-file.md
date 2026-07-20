# Download Live Audio File with Gladia

Retrieves a live transcription recording from Gladia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/live/:id/file`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Download Live Audio File](https://docs.gladia.io/api-reference/v2/live/get-audio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Gladia live job identifier. |
