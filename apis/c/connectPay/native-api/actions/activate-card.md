# Activate Card with ConnectPay

Activates a ChipAndPin card in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/activate`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Activate Card](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/activateCardByCardId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
