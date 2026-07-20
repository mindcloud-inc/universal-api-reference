# Query Explore Events with Sentry IO

Queries table-format explore events in Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/events/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Query Explore Events](https://docs.sentry.io/api/explore/query-explore-events-in-table-format/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `dataset` | query | `list` | yes | The Explore dataset to query, such as errors, transactions, spans, logs, or discover. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `field` | query | `string` | yes | A single Sentry Explore field, function, or equation to include in the table result. |
