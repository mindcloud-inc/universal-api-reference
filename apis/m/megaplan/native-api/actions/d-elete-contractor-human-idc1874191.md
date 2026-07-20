# Delete Contractor Human with Megaplan

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contractorHuman/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Delete Contractor Human](https://m60888876.megaplan.ru/api/v3/docs#contractorHumanid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Идентификатор контрагента |
| `body` | body | `object` | yes | Request body. RAML type: DeleteActionRequest |
