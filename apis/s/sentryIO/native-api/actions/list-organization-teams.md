# List Organization Teams with Sentry IO

Retrieves teams from a Sentry IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/teams/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Organization Teams](https://docs.sentry.io/api/teams/list-an-organizations-teams/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
