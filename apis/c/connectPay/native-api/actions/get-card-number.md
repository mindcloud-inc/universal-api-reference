# Get Card Number with ConnectPay

Retrieves an encrypted card number from ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/encryptedpan`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Card Number](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedPan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
