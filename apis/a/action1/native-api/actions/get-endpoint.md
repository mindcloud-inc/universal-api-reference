# Get Endpoint with Action1

Retrieves a managed endpoint from Action1 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/managed/:orgId/:endpointId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [Get Endpoint](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed_endpointId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
| `endpointId` | path | `string` | yes | Provide an endpoint ID. |
