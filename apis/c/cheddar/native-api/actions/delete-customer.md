# Delete Customer with Cheddar

Deletes an existing customer from Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/delete/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Delete Customer](https://docs.getcheddar.com/#delete-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
