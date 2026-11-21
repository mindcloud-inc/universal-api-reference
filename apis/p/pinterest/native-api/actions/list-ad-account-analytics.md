# List Ad Account Analytics with Pinterest

Retrieves paid ad spend and click metrics for a Pinterest ad account.

## Endpoint

- **Method:** `GET`
- **Path:** `ad_accounts/:adAccountId/analytics`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [List Ad Account Analytics](https://developers.pinterest.com/docs/api/v5/ad_account-analytics/)

## Requirements

- **OAuth scopes:** `ads:read`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | Enter the ID of the Pinterest ad account. |
| `columns` | query | `string` | yes | Enter comma-separated Pinterest metric names. The defaults are spend in micro-units and clicks on promoted Pins. Use OUTBOUND_CLICK_1 for clicks to a destination outside Pinterest. |
| `granularity` | query | `list<string>` | yes | Use DAY for daily results. Pinterest also supports TOTAL, HOUR, WEEK, and MONTH. Accepted values: `DAY`, `HOUR`, `MONTH`, `TOTAL`, `WEEK`. |
| `end_date` | query | `string` | yes | — |
| `start_date` | query | `string` | yes | — |
