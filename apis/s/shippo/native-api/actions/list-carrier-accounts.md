# List Carrier Accounts with Shippo - Legacy

Retrieves carrier accounts connected to your Shippo account.

## Endpoint

- **Method:** `GET`
- **Path:** `/carrier_accounts`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [List Carrier Accounts](https://docs.goshippo.com/docs/carriers/spec/carrier_acc/operation/ListCarrierAccounts/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `results` | query | `number` | no | Set how many carrier accounts to return per page. |
| `service_levels` | query | `boolean` | no | Include service levels for each returned carrier account. |
| `carrier` | query | `string` | no | Filter carrier accounts by carrier token. |
| `account_id` | query | `string` | no | Filter the response by carrier account ID. |
| `page` | query | `number` | no | Select which page of carrier accounts to return. |
| `apiKey` | path | `string` | no | Override the authentication API key here |
