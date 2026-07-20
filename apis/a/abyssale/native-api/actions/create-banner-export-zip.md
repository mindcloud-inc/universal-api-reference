# Create Banner Export ZIP with Abyssale

Exports Abyssale banners as a ZIP archive.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banners/export`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Create Banner Export ZIP](https://developers.abyssale.com/rest-api/image-export)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes |
| `callback_url` | body | `string` | yes |
