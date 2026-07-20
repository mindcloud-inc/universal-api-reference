# Add Custom Charge or Credit with Cheddar

Creates a custom charge or credit in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/add-charge/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Add Custom Charge or Credit](https://docs.getcheddar.com/#add-a-custom-charge-credit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `chargeCode` | body | `string` | yes | Code for the custom charge or credit. |
| `quantity` | body | `number` | yes | Positive integer quantity for the custom charge or credit. |
| `eachAmount` | body | `number` | yes | Positive or negative amount with two-digit decimal precision. |
| `description` | body | `string` | no | Description for the custom charge or credit. |
| `invoicePeriod` | body | `string` | no | Billing period: current (default) or outstanding. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
