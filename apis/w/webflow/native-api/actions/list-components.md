# List Components with Webflow

Retrieves a list of components from Webflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/components`
- **Base URL:** `https://api.webflow.com/v2`
- **Official documentation:** [List Components](https://developers.webflow.com/data/reference/pages-and-components/components/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | yes | Unique identifier for a Site. |
| `branchId` | query | `string` | no | Unique identifier for a branch. |
