# Create Invoice with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Invoice](https://m60888876.megaplan.ru/api/v3/docs#invoiceid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `string` | yes | Идентификатор счета, который необходимо обновить |
| `body` | body | `object` | yes | Required request body. RAML type: Invoice |
