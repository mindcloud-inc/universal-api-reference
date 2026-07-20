# Create Contractor Human with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/contractorHuman/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Contractor Human](https://m60888876.megaplan.ru/api/v3/docs#contractorHumanid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `string` | yes | Идентификатор контакта |
| `body` | body | `object` | yes | Required request body. RAML type: ContractorHuman |
