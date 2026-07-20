# List Endpoint Groups with Action1

Retrieves endpoint groups from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/groups/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Endpoint Groups](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_orgId)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
