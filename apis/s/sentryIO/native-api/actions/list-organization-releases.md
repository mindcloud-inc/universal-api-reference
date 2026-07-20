# List Organization Releases with Sentry IO

Retrieves releases from a Sentry IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/releases/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Organization Releases](https://docs.sentry.io/api/releases/list-an-organizations-releases/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
