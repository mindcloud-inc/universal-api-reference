# Get Endpoint Group with Action1

Retrieves an endpoint group from Action1 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoints/groups/:orgId/:groupId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [Get Endpoint Group](https://app.action1.com/apidocs/#/Endpoints.%20Endpoint%20Group%20Management/endpoints_groups_groupId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. |
| `groupId` | path | `string` | yes | Provide an endpoint group ID. |
