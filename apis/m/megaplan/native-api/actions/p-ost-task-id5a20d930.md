# Create Task with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Task](https://m60888876.megaplan.ru/api/v3/docs#taskid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Идентификатор задачи |
| `body` | body | `object` | yes | Required request body. RAML type: Task |
