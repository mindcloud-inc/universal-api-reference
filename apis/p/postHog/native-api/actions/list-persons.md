# List Persons with PostHog

Retrieves persons from a PostHog project.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments/:projectId/persons`
- **Base URL:** `https://us.posthog.com/api`
- **Official documentation:** [List Persons](https://posthog.com/docs/api/persons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | — |
| `projectId` | path | `list<number>` | yes | — |
| `properties[].key` | query | `string` | no | Key of the property you're filtering on. For example email or $current_url |
| `properties[].value` | query | `string` | no | Value of your filter. For example test@example.com or https://example.com/test/. Can be an array for an OR query, like ["test@example.com","ok@example.com"] |
| `properties[].operator` | query | `string` | no | Default: exact |
| `properties[].type` | query | `string` | no | Default: event |
| `created_at_from` | query | `string` | no | — |
| `distinct_id` | query | `string` | no | — |
| `properties[]` | query | `array` | no | — |
| `search` | query | `string` | no | — |
