# Create Pixel with TLY Link Shortener

Creates a new pixel in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/pixel`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Create Pixel](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The pixel display name. |
| `pixel_id` | body | `string` | yes | The provider pixel identifier. |
| `pixel_type` | body | `string` | yes | The pixel provider type. |
