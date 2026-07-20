# Modify a plan endpoint with xMatters

Updates a plan endpoint in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `plans/{planId}/endpoints`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Modify a plan endpoint](https://help.xmatters.com/xmapi/index.html#modify-a-plan-endpoint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `authentication` | body | `string` | no |
| `authenticationType` | body | `string` | no |
| `endpointType` | body | `string` | no |
| `id` | body | `string` | no |
| `name` | body | `string` | no |
| `planId` | path | `string` | no |
| `url` | body | `string` | no |
