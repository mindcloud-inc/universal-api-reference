# Get Pricing Plan with Cheddar

Retrieves pricing plan details from Cheddar.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/get/productCode/{productCode}/code/:planCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Get Pricing Plan](https://docs.getcheddar.com/#get-a-single-pricing-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Pricing plan code from Cheddar. |
