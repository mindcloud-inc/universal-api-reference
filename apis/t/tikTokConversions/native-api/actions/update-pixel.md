# Update Pixel with TikTok Conversions

Updates an existing Pixel in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/pixel/update/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Update Pixel](https://business-api.tiktok.com/portal/docs?id=1740858799524865)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advertiser_id` | body | `string` | yes |
| `pixel_id` | body | `string` | yes |
| `pixel_name` | body | `string` | yes |
| `advanced_matching_fields[]` | body | `array<string>` | no |
| `automatic_advanced_matching_fields[]` | body | `array<string>` | no |
