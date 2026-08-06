# Get Tax Code with Avalara AvaTax

## Endpoint

- **Method:** `GET`
- **Path:** `companies/:companyId/taxcodes/:id`
- **Base URL:** `{environment}`
- **Official documentation:** [Get Tax Code](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/TaxCodes/GetTaxCode/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | The ID of the company that owns this tax code. |
| `id` | path | `number` | yes | The numeric ID of the tax code to retrieve. |
