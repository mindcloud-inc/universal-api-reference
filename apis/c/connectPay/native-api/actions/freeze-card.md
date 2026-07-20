# Freeze Card with ConnectPay

Freezes an existing card in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/freeze`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Freeze Card](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/freezeCard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
