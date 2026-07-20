# List contributed conversions with Rakuten Advertising

Retrieves contributed conversions from Rakuten Advertising.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/publishers/contributed-conversions`
- **Base URL:** `https://api.linksynergy.com`
- **Official documentation:** [List contributed conversions](https://developers.rakutenadvertising.com/documentation/en-US/affiliate_apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `date` | yes | End date of conversion transaction date range in YYYY-MM-DD format. |
| `limit` | query | `number` | no | Number of records per page. Defaults to 1000. |
| `order_by` | query | `string` | no | Sort order: asc or desc. |
| `page` | query | `number` | no | Page number. Defaults to 1. |
| `sort_by` | query | `string` | no | Column to sort the contributed conversions by. Defaults to order date. |
| `start_date` | query | `date` | yes | Start date of conversion transaction date range in YYYY-MM-DD format. |
