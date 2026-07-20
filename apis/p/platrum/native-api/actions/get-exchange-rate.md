# Get exchange rate with Platrum

Retrieves a Platrum currency exchange rate by date.

## Endpoint

- **Method:** `POST`
- **Path:** `/finance/api/currency/exchange-rate`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Get exchange rate](http://api.docs.platrum.ru/modules/finance/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_code_from` | body | `string` | no | Source currency code. |
| `currency_code_to` | body | `string` | no | Target currency code. |
| `date` | body | `date` | no | Exchange-rate date. |
