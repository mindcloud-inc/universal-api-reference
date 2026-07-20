# Get BaaS Client Accounts with ConnectPay

Retrieves a BaaS client's accounts from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/baas/clients/:baasClientId/accounts`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get BaaS Client Accounts](https://docs.connectpay.com/docs/#tag/BaaS-Accounts/operation/getBaasClientAccountsByClientId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baasClientId` | path | `string` | no | BaaS client ID. |
