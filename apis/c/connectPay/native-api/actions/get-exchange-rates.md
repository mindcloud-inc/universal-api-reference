# Get Exchange Rates with ConnectPay

Retrieves currency exchange rates from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/currencyexchangerate`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Exchange Rates](https://docs.connectpay.com/docs/#tag/BaaS-FX-payments/operation/GetFxRates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencyPair` | query | `string` | no | Currency pair such as USDEUR. Multiple pairs may be provided when supported by ConnectPay. |
| `debtoraccountiban` | query | `string` | no | Payer account IBAN. |
