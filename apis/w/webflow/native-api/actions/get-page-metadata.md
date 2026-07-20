# Get Page Metadata with Webflow

Retrieves metadata for a page from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:page_id`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Get Page Metadata](https://developers.webflow.com/data/reference/pages-and-components/pages/get-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Unique identifier for a Page. |
| `localeId` | query | `string` | no | Unique identifier for a specific Locale. |
