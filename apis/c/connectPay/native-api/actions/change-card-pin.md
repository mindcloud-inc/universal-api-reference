# Change Card PIN with ConnectPay

Changes a ChipAndPin card PIN in ConnectPay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/baas/ob/cards/:cardId/pin`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Change Card PIN](https://docs.connectpay.com/docs/#tag/BaaS-Card-management/operation/changeCardPin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | no | Card ID. |
