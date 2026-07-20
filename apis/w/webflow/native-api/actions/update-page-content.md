# Update Page Content with Webflow

Updates static page content in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/:page_id/dom`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Update Page Content](https://developers.webflow.com/data/reference/pages-and-components/pages/update-static-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Unique identifier of the page. |
| `localeId` | query | `string` | yes | Locale identifier for the content update target. |
| `nodes[]` | body | `array<object>` | yes | Updated DOM nodes payload. |
