# List Organization Issues with Sentry IO

Retrieves issues from a Sentry IO organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/issues/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [List Organization Issues](https://docs.sentry.io/api/events/list-an-organizations-issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `query` | query | `string` | no | Optional Sentry structured search query. Leave blank for Sentry's default unresolved issue query; pass an empty query value to request all results. |
| `project` | query | `string` | no | Optional Sentry project ID. Sentry also accepts -1 for all available projects. |
| `statsPeriod` | query | `string` | no | Optional time range such as 24h, 7d, or 14d for issue stats. |
| `sort` | query | `list` | no | Optional Sentry issue sort such as date, freq, inbox, new, recommended, trends, or user. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `cursor` | query | `string` | no | Optional Sentry pagination cursor from the Link header. |
