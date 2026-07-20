# List Automation Schedules with Action1

Retrieves automation schedules from Action1 for an organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/schedules/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [List Automation Schedules](https://app.action1.com/apidocs/#/Automations.%20Schedules/policies_schedules_orgId_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Action1 organization ID. |
