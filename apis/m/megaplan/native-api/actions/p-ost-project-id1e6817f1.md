# Create Project with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Project](https://m60888876.megaplan.ru/api/v3/docs#projectid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Идентификатор проекта |
| `body` | body | `object` | yes | Required request body. RAML type: Project |
