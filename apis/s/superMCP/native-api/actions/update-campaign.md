# Update Campaign with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/campaign_update`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Update Campaign](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Ad platform data source code: AW, FA, AC, TIK, or LIA. |
| `account_id` | body | `string` | yes | Platform ad account ID from Discover Accounts. |
| `campaign_id` | body | `string` | yes | Campaign ID to update. |
| `name` | body | `string` | no | Updated campaign name. |
| `status` | body | `string` | no | Updated campaign status. |
| `budget_amount` | body | `number` | no | Updated budget amount in account currency. |
| `budget_type` | body | `string` | no | Updated budget type such as DAILY or LIFETIME. |
| `start_date` | body | `date` | no | Updated campaign start date. |
| `end_date` | body | `date` | no | Updated campaign end date. |
| `targeting` | body | `object` | no | Updated targeting object. |
| `platform_settings` | body | `object` | no | Updated platform-specific settings. |
| `bidding_strategy` | body | `string` | no | Updated bidding strategy. |
| `ad_groups[]` | body | `array<object>` | no | Ad groups or ad sets to add/update. |
