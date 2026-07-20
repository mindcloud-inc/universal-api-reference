# Unfreeze Card with ConnectPay

Unfreezes an existing card in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/unfreeze`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Unfreeze Card](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/unfreezeCard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
