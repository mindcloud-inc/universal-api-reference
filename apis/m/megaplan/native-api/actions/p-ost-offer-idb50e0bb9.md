# Create Offer with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Offer](https://m60888876.megaplan.ru/api/v3/docs#offerid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Id товара, который нужно обновить |
| `body` | body | `object` | yes | Required request body. RAML type: Offer |
