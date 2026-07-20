# List Organization Projects with Sentry IO

Retrieves projects from a Sentry IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/projects/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Organization Projects](https://docs.sentry.io/api/organizations/list-an-organizations-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
