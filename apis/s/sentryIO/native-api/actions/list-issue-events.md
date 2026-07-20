# List Issue Events with Sentry IO

Retrieves events for an issue in Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/issues/:issue_id/events/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Issue Events](https://docs.sentry.io/api/events/list-an-issues-events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `issue_id` | path | `string` | yes | The Sentry issue ID whose events should be listed. |
