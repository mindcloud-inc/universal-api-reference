# Get Team with Nozbe Personal

Retrieves a team from Nozbe Personal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Get Team](https://api4.nozbe.com/v1/api#/teams/getTeamById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team ID. |
| `fields` | query | `string` | no | Comma-separated fields to return. |
