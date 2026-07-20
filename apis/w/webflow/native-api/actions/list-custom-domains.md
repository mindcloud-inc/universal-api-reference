# List Custom Domains with Webflow

Retrieves custom domains for a site from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/custom_domains`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [List Custom Domains](https://developers.webflow.com/data/reference/sites/get-custom-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | Unique identifier for a Site. |
