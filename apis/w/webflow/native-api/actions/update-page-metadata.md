# Update Page Metadata with Webflow

Updates metadata for a page in Webflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pages/:page_id`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Update Page Metadata](https://developers.webflow.com/data/reference/pages-and-components/pages/update-page-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Unique identifier of the page. |
| `localeId` | query | `string` | no | Optional locale identifier for localized page metadata updates. |
| `title` | body | `string` | no | Updated page title. |
| `slug` | body | `string` | no | Updated page slug. |
| `seo` | body | `object` | no | SEO settings payload. |
| `openGraph` | body | `object` | no | Open Graph settings payload. |
