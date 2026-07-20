# List Organization Members with Sentry IO

Retrieves members from a Sentry IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/members/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Organization Members](https://docs.sentry.io/api/organizations/list-an-organizations-members/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
