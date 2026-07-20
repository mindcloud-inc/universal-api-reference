# Update Subscription Card By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/cards/:cardId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Subscription Card By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cardId` | path | `string` | yes | Coast card ID of the card to update. |
| `status` | body | `list` | no | Updated status for the card. Accepted values: `0`, `1`, `2`, `3`. |
| `name` | body | `string` | no | Updated name for the card. |
| `primaryPersonId` | body | `string` | no | Coast person ID whose name appears on purchases for this card. |
| `otherPersonIds[]` | body | `array<string>` | no | Other Coast people allowed to use this card in addition to the primary person. |
| `sharedByPersonId` | body | `string` | no | Coast person ID of the person sharing this card. |
| `spendLimit` | body | `object` | no | Updated spending limits for the card. |
| `requestReceipts` | body | `boolean` | no | Whether this card should require receipts. |
| `requestMemos` | body | `boolean` | no | Whether this card should require memos. |
