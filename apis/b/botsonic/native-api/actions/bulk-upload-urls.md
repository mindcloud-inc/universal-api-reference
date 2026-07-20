# Bulk Upload URLs with Botsonic

Uploads multiple URLs as bot data in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-data/bulk-upsert-urls`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [Bulk Upload URLs](https://docs.botsonic.com/reference/bulk_upload_urls_v1_business_bot_data_bulk_upsert_urls_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | URLs to upload or upsert for bot training. |
| `sitemap_id` | body | `string` | no | Optional sitemap identifier. |
| `is_sitemap` | body | `boolean` | no | Whether the uploaded URLs represent a sitemap. |
| `sitemap_root` | body | `string` | no | Optional sitemap root URL. |
| `ability_id` | body | `string` | no | Optional ability identifier. |
| `is_crawled` | body | `boolean` | no | Whether the URLs have already been crawled. |
