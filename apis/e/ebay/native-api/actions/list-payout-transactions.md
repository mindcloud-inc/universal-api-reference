# List Payout Transactions with eBay

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction`
- **Base URL:** `https://apiz.ebay.com/sell/finances/v1`
- **API:** Sell Finances
- **Official documentation:** [List Payout Transactions](https://developer.ebay.com/develop/api/sell/finances_api/transaction/getTransactions)

## Requirements

- **OAuth scopes:** `https://api.ebay.com/oauth/api_scope/sell.finances`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payoutId` | query | `string` | yes |
