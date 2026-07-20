# Get Account Usage with Crawlbase

Retrieves account usage statistics from Crawlbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/account`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [Get Account Usage](https://crawlbase.com/docs/account-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product` | query | `list` | yes | Crawlbase product to report usage for. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `previous_month` | query | `boolean` | no | Set true to include current and previous month statistics. |
