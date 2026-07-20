# List Balances with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/user/balances`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [List Balances](https://api.gainium.io/api/docs/v2#/User/getUserBalances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset` | query | `string` | no | Limit balances to one asset symbol. |
| `assets` | query | `string` | no | Limit balances to multiple asset symbols. |
| `exchangeId` | query | `string` | no | Limit balances to one exchange ID. |
| `fields` | query | `string` | no | Field selection preset or custom field list. |
