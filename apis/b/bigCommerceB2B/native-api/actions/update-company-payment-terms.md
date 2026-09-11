# Update Company Payment Terms with BigCommerce (B2B)

## Endpoint

- **Method:** `PUT`
- **Path:** `companies/:companyId/payment-terms`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Update Company Payment Terms](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `string` | yes |
| `isEnabled` | body | `boolean` | no |
| `paymentTerms` | body | `number` | no |
