# Download Music with Freepik

Retrieves a Freepik music download URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/music/{{music-id}}/download`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Download Music](https://docs.freepik.com/api-reference/music/download-music)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `music-id` | path | `number` | yes | Freepik music track identifier to download. |
