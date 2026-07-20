# List Workflow Runs with Skyvern

Retrieves workflow runs for your organization from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workflows/runs`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [List Workflow Runs](https://www.skyvern.com/docs/api-reference/workflows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `error_code` | query | `string` | no | Exact-match filter on task error_code values. |
| `search_key` | query | `string` | no | Case-insensitive substring search across run metadata. |
| `status` | query | `string` | no | Filter by one or more run statuses. |
