# Get Component Content with Webflow

Retrieves content for a component from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/components/:component_id/dom`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Get Component Content](https://developers.webflow.com/data/reference/pages-and-components/components/get-content)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | The unique identifier of the site. |
| `component_id` | path | `string` | yes | The unique identifier of the component. |
| `localeId` | query | `string` | no | The locale identifier for localized content. |
| `branchId` | query | `string` | no | The branch identifier for branch content. |
| `limit` | query | `number` | no | Maximum number of content nodes to return. |
| `offset` | query | `number` | no | Number of content nodes to skip before returning results. |
