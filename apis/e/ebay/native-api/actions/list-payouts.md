# List Payouts with eBay

## Endpoint

- **Method:** `GET`
- **Path:** `/payout`
- **Base URL:** `https://apiz.ebay.com/sell/finances/v1`
- **API:** Sell Finances
- **Official documentation:** [List Payouts](https://developer.ebay.com/develop/api/sell/finances_api/payout/getPayouts)

## Requirements

- **OAuth scopes:** `https://api.ebay.com/oauth/api_scope/sell.finances`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Filter by payout status or payout date using eBay’s syntax. Example: payoutStatus:{SUCCEEDED}. |
| `sort` | query | `string` | no | Use payoutDate to show oldest payouts first. eBay returns the newest payouts first by default. |
