# Get BaaS Merchant Providers with ConnectPay

Retrieves BaaS merchant providers from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/baas/merchant/brands/:BaaSClientBrandId/providers`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get BaaS Merchant Providers](https://docs.connectpay.com/docs/#tag/BaaS-Merchant-payments-and-providers/operation/GetProviders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BaaSClientBrandId` | path | `string` | no | Merchant brand identifier provided by ConnectPay. |
| `countryCode` | query | `string` | no | Provider country code, for example DE, NL, or LT. |
