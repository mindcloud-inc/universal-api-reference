# List Pages with Webflow

Retrieves a list of pages from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/pages`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [List Pages](https://developers.webflow.com/data/reference/pages-and-components/pages/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | Unique identifier for a Site. |
| `localeId` | query | `string` | no | Unique identifier for a specific Locale. |
