# Create Deal with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/deal/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Deal](https://m60888876.megaplan.ru/api/v3/docs#dealid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Идентификатор процесса |
| `body` | body | `object` | yes | Required request body. RAML type: Deal |
