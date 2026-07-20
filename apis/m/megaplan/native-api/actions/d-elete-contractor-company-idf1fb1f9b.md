# Delete Contractor Company with Megaplan

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contractorCompany/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Delete Contractor Company](https://m60888876.megaplan.ru/api/v3/docs#contractorCompanyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter from Megaplan RAML. |
| `id` | query | `number` | yes | Идентификатор контрагента |
| `body` | body | `object` | yes | Request body. RAML type: DeleteActionRequest |
