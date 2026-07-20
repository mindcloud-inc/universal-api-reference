# Get Project with Teamdeck

Retrieves a project from your Teamdeck organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Get Project](https://teamdeck.io/developers/api#operation/projectDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck project ID. |
| `expand` | query | `string` | no | — |
