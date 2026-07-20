# Get Card Authorisation Details with ConnectPay

Retrieves card authorisation details from ConnectPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/baas/ob/cards/:cardId/authorisation/:authorisationId`
- **Base URL:** `https://api-stage.connectpay.com`
- **Official documentation:** [Get Card Authorisation Details](https://docs.connectpay.com/docs/#tag/BaaS-Card-creation-and-details/operation/getCardAuthorisationById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorisationId` | path | `string` | no | Card authorisation ID. |
| `cardId` | path | `string` | no | Card ID. |
