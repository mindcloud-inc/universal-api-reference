# List Endpoints with Action1

Retrieves managed endpoints from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/managed/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Endpoints](https://app.action1.com/apidocs/#/Endpoints/endpoints_managed)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
