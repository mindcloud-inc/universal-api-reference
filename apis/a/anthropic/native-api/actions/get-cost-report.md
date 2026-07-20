# Get Cost Report with Anthropic

Retrieves the current Anthropic cost report.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/cost_report`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Get Cost Report](https://platform.claude.com/docs/en/api/admin/cost_report/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starting_at` | query | `string` | yes | Start timestamp (inclusive) for the report window. |
| `ending_at` | query | `string` | no | End timestamp (exclusive) for the report window. |
| `bucket_width` | query | `string` | no | Aggregation bucket width. |
| `group_by` | query | `list<string>` | no | Dimensions used to group costs. |
| `workspace_ids` | query | `list<string>` | no | Filter by workspace IDs. |
| `api_key_ids` | query | `list<string>` | no | Filter by API key IDs. |
| `limit` | query | `number` | no | Number of rows per page. |
| `page` | query | `number` | no | Page number for pagination. |
