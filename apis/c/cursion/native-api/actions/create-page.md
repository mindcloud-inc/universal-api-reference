# Create Page with Cursion

Creates a new page in Cursion.

## Endpoint

- **Method:** `POST`
- **Path:** `/page`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [Create Page](https://docs.cursion.dev/api/page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_url` | body | `string` | yes | The page URL to monitor. |
| `site_id` | body | `string` | yes | The parent site identifier. |
