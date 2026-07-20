# List Transactions by Account with Outseta

Retrieves account transactions from Outseta.

## Endpoint

- **Method:** `GET`
- **Path:** `/billing/transactions/:accountUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [List Transactions by Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
