# Update Company Credit with BigCommerce (B2B)

## Endpoint

- **Method:** `PUT`
- **Path:** `companies/:companyId/credit`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Update Company Credit](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `availableCredit` | body | `number` | no | — |
| `creditCurrency` | body | `string` | no | — |
| `creditHold` | body | `boolean` | no | Format: `toggle`. |
| `limitPurchases` | body | `boolean` | no | Format: `toggle`. |
| `companyId` | path | `string` | yes | — |
| `creditEnabled` | body | `boolean` | no | Format: `toggle`. |
