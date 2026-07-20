# List Automation Instances with Action1

Retrieves automation instances from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/instances/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Automation Instances](https://app.action1.com/apidocs/#/Automations.%20Instances/policies_instances_orgId_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
