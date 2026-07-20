# Get Customer with Cheddar

Retrieves customer billing details from Cheddar.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/get/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Get Customer](https://docs.getcheddar.com/#get-a-single-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
