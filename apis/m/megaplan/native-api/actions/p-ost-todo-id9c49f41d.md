# Create Todo with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/todo/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Todo](https://m60888876.megaplan.ru/api/v3/docs#todoid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | NO_DESCRIPTION |
| `body` | body | `object` | yes | Required request body. RAML type: Todo |
