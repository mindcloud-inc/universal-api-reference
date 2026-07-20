# List Endpoint Missing Updates with Action1

Retrieves missing updates from Action1 for a specific endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/managed/:orgId/:endpointId/missing-updates`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Endpoint Missing Updates](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed_endpointId_missing_updates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
| `endpointId` | path | `string` | yes | Managed endpoint ID. |
