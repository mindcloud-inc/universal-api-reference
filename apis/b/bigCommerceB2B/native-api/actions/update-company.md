# Update Company with BigCommerce (B2B)

## Endpoint

- **Method:** `PUT`
- **Path:** `companies/:companyId`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Update Company](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `string` | yes |
| `extraFields[].fieldName` | body | `string` | no |
| `extraFields[]` | body | `array` | no |
| `extraFields[].fieldValue` | body | `string` | no |
