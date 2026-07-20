# List Accounts with Billage

Retrieves account records from Billage by criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/accounts`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [List Accounts](https://app.getbillage.com/api/documentation.html#/Accounts/accountsByParameters)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search accounts |
| `type` | query | `string` | no | Filter by account type |
| `alias` | query | `string` | no | Filter by account alias |
| `name` | query | `string` | no | Filter by account name |
| `vat` | query | `string` | no | Filter by VAT number |
| `fields` | query | `string` | no | Limit returned account fields |
| `colour` | query | `string` | no | Filter by colour |
| `owner` | query | `string` | no | Filter by owner |
| `address` | query | `string` | no | Filter by address |
| `country` | query | `string` | no | Filter by country |
| `date-from` | query | `string` | no | Filter accounts modified after this date |
| `date-to` | query | `string` | no | Filter accounts modified before this date |
