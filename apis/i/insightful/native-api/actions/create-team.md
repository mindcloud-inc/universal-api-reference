# Create Team with Insightful

Creates a new team in your Insightful account.

## Endpoint

- **Method:** `POST`
- **Path:** `/team`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Create Team](https://developers.insightful.io/#6ad29832-4a3f-4af4-8138-c7ede6ab847b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | A description for the team. |
| `name` | body | `string` | yes | The team name. |
