# Get BaaS Client Account Details with ConnectPay

Retrieves a BaaS client's account details from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/baas/clients/:baasClientId/accounts/:accountId`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get BaaS Client Account Details](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getAccountDetailsByAccountId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | ID of the account. |
| `baasClientId` | path | `string` | no | BaaS client ID. |
