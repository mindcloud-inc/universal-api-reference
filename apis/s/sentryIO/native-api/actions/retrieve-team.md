# Retrieve Team with Sentry IO

Retrieves a team from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:organization_id_or_slug/:team_id_or_slug/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Team](https://docs.sentry.io/api/teams/retrieve-a-team/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `team_id_or_slug` | path | `string` | yes | The Sentry team ID or slug. |
