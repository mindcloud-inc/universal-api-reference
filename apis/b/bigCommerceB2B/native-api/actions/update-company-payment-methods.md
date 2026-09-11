# Update Company Payment Methods with BigCommerce (B2B)

## Endpoint

- **Method:** `PUT`
- **Path:** `companies/:companyId/payments`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Update Company Payment Methods](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/payment#update-company-credit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `string` | yes |
| `payments[].code` | body | `string` | no |
| `payments[]` | body | `array` | no |
| `payments[].isEnabled` | body | `boolean` | no |
