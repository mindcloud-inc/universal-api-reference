# Block Account with ConnectPay

Blocks an existing account in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/accounts/:accountId/block`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Block Account](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/blockAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | ID of the account. |
