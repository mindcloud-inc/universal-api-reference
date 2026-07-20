# Update Prompt (partial) with Statsig

Updates a prompt in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/prompts/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Prompt (partial)](https://docs.statsig.com/api-reference/prompts/update-prompt-partial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `description` | body | `string` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
