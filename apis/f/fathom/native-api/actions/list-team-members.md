# List Team Members with Fathom

Retrieves team members from Fathom.

## Endpoint

- **Method:** `GET`
- **Path:** `/team_members`
- **Base URL:** `https://api.fathom.ai/external/v1`
- **Official documentation:** [List Team Members](https://developers.fathom.ai/api-reference/team-members/list-team-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `string` | no | Filter team members by team name. |
| `cursor` | query | `string` | no | Pagination cursor. |
