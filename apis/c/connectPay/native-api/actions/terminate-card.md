# Terminate Card with ConnectPay

Terminates an existing card in ConnectPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/baas/ob/cards/:cardId/close`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Terminate Card](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/terminateCard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
