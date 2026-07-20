# Create Contractor Company with Megaplan

## Endpoint

- **Method:** `POST`
- **Path:** `/contractorCompany/:id`
- **Base URL:** `https://m60888876.megaplan.ru/api/v3`
- **Official documentation:** [Create Contractor Company](https://m60888876.megaplan.ru/api/v3/docs#contractorCompanyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required path parameter from Megaplan RAML. |
| `id` | query | `string` | yes | Идентификатор контакта-компании |
| `body` | body | `object` | yes | Required request body. RAML type: ContractorCompany |
