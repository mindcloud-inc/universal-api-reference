# Get forms in a plan with xMatters

Retrieves forms in a plan from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `plans/{planId}/forms`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get forms in a plan](https://help.xmatters.com/xmapi/index.html#get-forms-in-a-plan)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `embed` | query | `string` | no |
| `planId` | path | `string` | no |
