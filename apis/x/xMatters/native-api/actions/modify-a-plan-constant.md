# Modify a plan constant with xMatters

Updates a plan constant in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/constants`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a plan constant](https://help.xmatters.com/xmapi/index.html#modify-a-plan-constant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `id` | body | `string` | no |
| `name` | body | `string` | no |
| `planId` | path | `string` | no |
| `value` | body | `string` | no |
