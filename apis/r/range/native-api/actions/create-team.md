# Create Team with Range

Create a new team with optional parent and mascot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/teams`
- **Base URL:** `https://api.range.co`
- **Official documentation:** [Create Team](https://www.range.co/docs/api#rpc-create-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The team's charter or purpose. |
| `mascot` | body | `string` | no | An emoji-one code such as :bear:. |
| `name` | body | `string` | no | The team's name. |
| `parent_id` | body | `string` | no | Parent team ID. Leave empty for a root team. |
| `slug` | body | `string` | no | Unique URL slug for the team. |
