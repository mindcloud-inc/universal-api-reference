# Get Encrypted PIN with ConnectPay

Retrieves an encrypted ChipAndPin card PIN from ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/encryptedpin`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Encrypted PIN](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardEncryptedPin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
