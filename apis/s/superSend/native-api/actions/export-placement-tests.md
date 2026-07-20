# Export Placement Tests with SuperSend

Creates a placement test export in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/placement-tests/export`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Export Placement Tests](https://docs.supersend.io/docs/placement-test)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | body | `string` | yes | — |
| `filters` | body | `object` | no | — |
| `filters.search` | body | `string` | no | — |
| `filters.status` | body | `string` | no | — |
| `filters.conditional_filters` | body | `string` | no | — |
| `filters.sortBy` | body | `string` | no | — |
| `filters.sortOrder` | body | `string` | no | Allowed values: asc, desc. |
