# List Endpoint Installed Software Rows with Action1

Retrieves installed software rows from Action1 for a specific endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/installed-software/:orgId/data/:endpointId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Endpoint Installed Software Rows](https://app.action1.com/apidocs/#/Software%20Deployment.%20Installed%20Software%20Inventory/apps_orgId_data_endpointId_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
| `endpointId` | path | `string` | yes | Managed endpoint ID. |
