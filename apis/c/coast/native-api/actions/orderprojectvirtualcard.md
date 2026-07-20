# Order Project Virtual Card with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/cards/virtual`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Order Project Virtual Card](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the card. |
| `projectBudgetId` | body | `string` | yes | Coast project budget ID permanently assigned to this card. |
| `primaryPersonId` | body | `string` | yes | Coast person ID whose name appears on purchases for this card. |
| `spendLimit` | body | `object` | yes | Spending limits for this card. |
