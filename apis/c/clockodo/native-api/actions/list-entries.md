# List Entries with Clockodo

Retrieves time entries from your Clockodo account.

## Endpoint

- **Method:** `GET`
- **Path:** `/entries`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [List Entries](https://www.clockodo.com/en/api/entries/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calc_also_revenues_for_projects_with_hard_budget` | query | `boolean` | no | — |
| `enhanced_list` | query | `boolean` | no | — |
| `filter[billable]` | query | `number` | no | — |
| `filter[budget_type]` | query | `string` | no | — |
| `filter[customers_id]` | query | `string` | no | — |
| `filter[lumpsum_services_id]` | query | `string` | no | — |
| `filter[projects_id]` | query | `string` | no | — |
| `filter[services_id]` | query | `string` | no | — |
| `filter[text]` | query | `string` | no | — |
| `filter[texts_id]` | query | `string` | no | — |
| `filter[users_id]` | query | `string` | no | — |
| `time_since` | query | `string` | yes | Start of the time range in ISO 8601 UTC. |
| `time_until` | query | `string` | yes | End of the time range in ISO 8601 UTC. |
