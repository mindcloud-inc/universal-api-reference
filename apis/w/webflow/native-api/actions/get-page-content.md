# Get Page Content with Webflow

Retrieves static page content from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:page_id/dom`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Get Page Content](https://developers.webflow.com/data/reference/pages-and-components/pages/get-content)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Unique identifier for a Page. |
| `localeId` | query | `string` | no | Unique identifier for a specific Locale. |
