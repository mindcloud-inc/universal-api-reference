# Update Agent with Callingly

Updates an agent in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/agents/{{id}}`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Update Agent](https://help.callingly.com/article/38-callingly-api-documentation#update-agent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `account_id` | body | `string` | no |
| `fname` | body | `string` | no |
| `lname` | body | `string` | no |
| `phone_number` | body | `string` | no |
| `ext` | body | `string` | no |
| `timezone` | body | `string` | no |
| `donotdisturb` | body | `string` | no |
| `donotdisturb_until` | body | `string` | no |
