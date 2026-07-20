# Create a plan form with xMatters

Creates a plan form in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/forms`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a plan form](https://help.xmatters.com/xmapi/index.html#create-a-plan-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `name` | body | `string` | no |
| `planId` | path | `string` | no |
