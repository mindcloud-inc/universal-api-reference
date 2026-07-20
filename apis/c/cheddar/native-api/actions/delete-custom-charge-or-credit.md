# Delete Custom Charge or Credit with Cheddar

Deletes a custom charge or credit from Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/delete-charge/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Delete Custom Charge or Credit](https://docs.getcheddar.com/#delete-a-custom-charge-credit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `chargeId` | body | `string` | yes | Cheddar ID for the charge or credit to remove. |
| `invoicePeriod` | body | `string` | no | Billing period: current (default) or outstanding. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
