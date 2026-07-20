# Get BaaS Clients with ConnectPay

Retrieves BaaS clients from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/ob/baas/clients`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get BaaS Clients](https://docs.connectpay.com/docs/#tag/BaaS-Clients/operation/getBaaSClients)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baasClientId` | query | `string` | no | Optional BaaS client ID filter. |
| `baasClientStatus` | query | `string` | no | Optional BaaS client status filter. |
| `customerName` | query | `string` | no | Optional BaaS customer name fragment filter. |
