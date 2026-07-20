# Download Icon with Freepik

Retrieves a Freepik icon download URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/icons/{{id}}/download`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Download Icon](https://docs.freepik.com/api-reference/icons/download-an-icon)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Freepik icon identifier to download. |
| `format` | query | `list` | no | Icon download format. PNG is verified with the current credential. Accepted values: `png`. |
| `png_size` | query | `number` | no | PNG size in pixels when format is png. |
