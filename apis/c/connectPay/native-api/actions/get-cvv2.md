# Get CVV2 with ConnectPay

Retrieves an encrypted card CVV2 from ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/encryptedcvv2`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get CVV2](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedCvv2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
