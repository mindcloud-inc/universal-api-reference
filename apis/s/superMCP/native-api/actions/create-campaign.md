# Create Campaign with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/campaign_create`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Create Campaign](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Ad platform data source code: AW, FA, AC, TIK, or LIA. |
| `account_id` | body | `string` | yes | Platform ad account ID from Discover Accounts. |
| `name` | body | `string` | yes | Campaign name. |
| `status` | body | `string` | no | Campaign status. Supermetrics creates campaigns as PAUSED for safe review. |
| `budget_amount` | body | `number` | no | Budget amount in account currency. |
| `budget_type` | body | `string` | no | Budget type such as DAILY or LIFETIME. |
| `start_date` | body | `date` | no | Campaign start date in YYYY-MM-DD format. |
| `end_date` | body | `date` | no | Campaign end date in YYYY-MM-DD format. |
| `targeting` | body | `object` | no | Campaign-level targeting object. |
| `platform_settings` | body | `object` | no | Platform-specific campaign settings. |
| `bidding_strategy` | body | `string` | no | Platform bidding strategy. |
| `ad_groups[]` | body | `array<object>` | no | Ad groups or ad sets to create with the campaign. |
