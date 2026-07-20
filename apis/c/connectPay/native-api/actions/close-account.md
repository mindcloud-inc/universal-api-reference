# Close Account with ConnectPay

Closes an existing IBAN account in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/accounts/:accountId/close`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Close Account](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/closeIBANAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | ID of the account. |
