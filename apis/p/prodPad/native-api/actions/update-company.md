# Update Company with ProdPad

Updates an existing company in ProdPad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:id`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Update Company](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Feedback/PutCompany)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the company to edit. |
| `name` | body | `string` | no | Name of the company. |
| `city` | body | `string` | no | City the company is located in or tagged with. |
| `country` | body | `string` | no | ISO Alpha-2 country code. |
| `size` | body | `string` | no | Company size by employee band. |
| `value` | body | `string` | no | Business value of the company. |
