# Create Agent with Callingly

Creates an agent in Callingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Create Agent](https://help.callingly.com/article/38-callingly-api-documentation#create-agent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | body | `string` | no |
| `ext` | body | `string` | no |
| `timezone` | body | `string` | no |
| `fname` | body | `string` | yes |
| `lname` | body | `string` | yes |
| `phone_number` | body | `string` | yes |
