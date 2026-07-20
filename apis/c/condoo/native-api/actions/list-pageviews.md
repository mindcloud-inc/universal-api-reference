# List Pageviews with condoo

Retrieves pageviews from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/pageviews-lightweight/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Pageviews](https://trk.condoo.systems/en/api-documentation/pageviews-lightweight)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browser_language` | query | `string` | no | Filter pageviews by browser language. |
| `browser_timezone` | query | `string` | no | Filter pageviews by browser timezone. |
| `continent_code` | query | `string` | no | Optional continent code selector. |
| `country_code` | query | `string` | no | Optional country code selector. |
| `device_type` | query | `string` | no | Optional device type. Allowed values: desktop, tablet, mobile. |
| `search` | query | `string` | no | Optional search string. |
| `search_by` | query | `string` | no | Optional search field. Allowed values: path, referrer_host. |
| `theme` | query | `string` | no | Optional theme. Allowed values: light, dark. |
| `type` | query | `string` | no | Optional pageview type. Allowed values: pageview, custom. |
| `website_id` | query | `number` | no | Optional website ID selector. |
