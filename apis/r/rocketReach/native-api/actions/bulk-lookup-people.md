# Bulk Lookup People with RocketReach

Creates a RocketReach bulk people lookup.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulkLookup`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Bulk Lookup People](https://docs.rocketreach.co/reference/bulk-person-lookup-person-lookup-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_employer` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `id` | body | `number` | no | — |
| `linkedin_url` | body | `string` | no | — |
| `lookup_type` | body | `string` | no | Lookup type for the person lookup query. |
| `name` | body | `string` | no | — |
| `npi_number` | body | `number` | no | National Provider Identifier for the person lookup query. |
| `profile_list` | body | `string` | no | — |
| `queries[]` | body | `array<object>` | no | List of profile lookup queries for between 10 and 100 profiles. |
| `title` | body | `string` | no | Job title for the person lookup query. |
| `webhook_id` | body | `number` | no | — |
