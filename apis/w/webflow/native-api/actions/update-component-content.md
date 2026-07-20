# Update Component Content with Webflow

Updates content for a component in Webflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/components/:component_id/dom`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Update Component Content](https://developers.webflow.com/data/reference/pages-and-components/components/update-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | The unique identifier of the site. |
| `component_id` | path | `string` | yes | The unique identifier of the component. |
| `localeId` | query | `string` | no | The locale identifier for localized content. |
| `branchId` | query | `string` | no | The branch identifier for branch content. |
| `nodes` | body | `list<object>` | yes | List of component DOM nodes to update. |
