# Update Personalized Card By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/cards/:cardId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Personalized Card By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | Coast card ID of the card to update. |
| `status` | body | `list` | no | Updated status for the card. Accepted values: `active`, `cancelled`, `frozen`, `locked`. |
