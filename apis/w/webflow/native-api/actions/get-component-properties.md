# Get Component Properties with Webflow

Retrieves properties for a component from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/components/:component_id/properties`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [Get Component Properties](https://developers.webflow.com/data/reference/pages-and-components/components/get-properties)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | The unique identifier of the site. |
| `component_id` | path | `string` | yes | The unique identifier of the component. |
| `localeId` | query | `string` | no | The locale identifier for localized properties. |
| `branchId` | query | `string` | no | The branch identifier for branch content. |
| `limit` | query | `number` | no | Maximum number of properties to return. |
| `offset` | query | `number` | no | Number of properties to skip before returning results. |
