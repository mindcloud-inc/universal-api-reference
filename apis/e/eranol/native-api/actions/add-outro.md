# Add Outro with Eranol

Creates an outro addition job in Eranol.

## Endpoint

- **Method:** `POST`
- **Path:** `/ffmpeg/video/add-outro`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Add Outro](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source video URL |
| `outro_url` | body | `string` | yes | Outro clip URL |
