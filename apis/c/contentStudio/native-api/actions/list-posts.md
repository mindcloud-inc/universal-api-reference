# List Posts with ContentStudio

Retrieves social media posts for a ContentStudio workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace_id/posts`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [List Posts](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approval_assigned_to[]` | query | `array<string>` | no | Filter posts assigned to one or more approver user IDs. |
| `approval_requested_by[]` | query | `array<string>` | no | Filter posts requested for approval by one or more user IDs. |
| `date_from` | query | `date` | no | Filter posts from this date (YYYY-MM-DD). |
| `date_to` | query | `date` | no | Filter posts through this date (YYYY-MM-DD). |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of items per page. |
| `status[]` | query | `array<string>` | no | Filter posts by one or more status values. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
