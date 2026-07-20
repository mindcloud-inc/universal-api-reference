# Create Prompt with Statsig

Creates a prompt in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/prompts`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Prompt](https://docs.statsig.com/api-reference/prompts/create-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `displayName` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `creatorID` | body | `string` | no | Request body field. |
| `owner` | body | `object` | no | Request body field. |
| `creatorEmail` | body | `string` | no | Request body field. |
