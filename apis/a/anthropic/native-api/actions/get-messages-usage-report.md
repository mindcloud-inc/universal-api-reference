# Get Messages Usage Report with Anthropic

Retrieves the Anthropic messages usage report.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/organizations/usage_report/messages`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Get Messages Usage Report](https://platform.claude.com/docs/en/api/admin/usage_report/retrieve_messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starting_at` | query | `string` | yes | Start timestamp (inclusive) for the report window. |
| `ending_at` | query | `string` | no | End timestamp (exclusive) for the report window. |
| `bucket_width` | query | `string` | no | Aggregation bucket width. |
| `group_by` | query | `list<string>` | no | Dimensions used to group usage metrics. |
| `workspace_ids` | query | `list<string>` | no | Filter by workspace IDs. |
| `api_key_ids` | query | `list<string>` | no | Filter by API key IDs. |
| `model` | query | `string` | no | Filter by model name. |
| `limit` | query | `number` | no | Number of rows per page. |
| `page` | query | `number` | no | Page number for pagination. |
