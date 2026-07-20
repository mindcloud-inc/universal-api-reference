# List Team Members with Sentry IO

Retrieves members from a Sentry IO team.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:organization_id_or_slug/:team_id_or_slug/members/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Team Members](https://docs.sentry.io/api/teams/list-a-teams-members/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `team_id_or_slug` | path | `string` | yes | The Sentry team ID or slug. |
