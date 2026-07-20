# Order Subscription Virtual Card with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/cards/virtual`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Order Subscription Virtual Card](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the card. |
| `creatorPersonId` | body | `string` | yes | Coast person ID of the person creating this card. |
| `primaryPersonId` | body | `string` | yes | Coast person ID whose name appears on purchases for this card. |
| `otherPersonIds[]` | body | `array<string>` | yes | Other Coast people allowed to use this card in addition to the primary person. |
| `spendLimit` | body | `object` | yes | Spending limits for this card. |
| `requestReceipts` | body | `boolean` | yes | Whether this card should require receipts. |
| `requestMemos` | body | `boolean` | yes | Whether this card should require memos. |
