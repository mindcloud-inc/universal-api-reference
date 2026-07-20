# Exchange FSPay Payment Account with Launch27

Exchanges an FSPay payment account in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `fspay/token/exchange`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Exchange FSPay Payment Account](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hosted_payment_account_id` | body | `string` | yes | Hosted payment account ID returned by FullSteam hosted payments. |
