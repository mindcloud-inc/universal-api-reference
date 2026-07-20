# Update Component Properties with Webflow

Updates properties for a component in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/components/:component_id/properties`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Update Component Properties](https://developers.webflow.com/data/reference/pages-and-components/components/update-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | The unique identifier of the site. |
| `component_id` | path | `string` | yes | The unique identifier of the component. |
| `localeId` | query | `string` | no | The locale identifier for localized properties. |
| `branchId` | query | `string` | no | The branch identifier for branch content. |
| `properties` | body | `list<object>` | yes | List of component properties to update. |
