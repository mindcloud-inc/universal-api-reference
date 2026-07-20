# List Endpoint Group Contents with Action1

Retrieves endpoint group contents from Action1 by group ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/groups/:orgId/:groupId/contents`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Endpoint Group Contents](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_groupId_contents_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
| `groupId` | path | `string` | yes | Endpoint group ID. |
