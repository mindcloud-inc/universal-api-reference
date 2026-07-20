# Publish Site with Webflow

Publishes a site in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/publish`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Publish Site](https://developers.webflow.com/data/reference/sites/publish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | Unique identifier of the site. |
| `customDomains[]` | body | `array<string>` | no | Optional list of custom domain IDs to publish. |
| `publishToWebflowSubdomain` | body | `boolean` | no | Set true to publish to the Webflow subdomain. |
