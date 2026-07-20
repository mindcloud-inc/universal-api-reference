# Replace Team Agents with Callingly

Updates team agents in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/teams/{{id}}/agents`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Replace Team Agents](https://help.callingly.com/article/38-callingly-api-documentation#update-users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `agents[]` | body | `array<string>` | yes |
