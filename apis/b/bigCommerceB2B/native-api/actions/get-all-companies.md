# Get All Companies with BigCommerce (B2B)

## Endpoint

- **Method:** `GET`
- **Path:** `companies`
- **Base URL:** `https://api-b2b.bigcommerce.com/api/v3/io/`
- **Official documentation:** [Get All Companies](https://developer.bigcommerce.com/b2b-edition/apis/rest-management/company/companies)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyStatus` | query | `number` | no |
| `limit` | query | `number` | no |
| `include` | query | `string` | no |
| `bcGroupId` | query | `string` | no |
| `bcOrderId` | query | `number` | no |
| `customerId` | query | `number` | no |
| `extraFieldFilterType` | query | `string` | no |
| `extraFields[]` | query | `array` | no |
| `isIncludeExtraFields` | query | `string` | no |
| `maxCreated` | query | `number` | no |
| `maxModified` | query | `number` | no |
| `minCreated` | query | `number` | no |
| `minModified` | query | `number` | no |
| `orderBy` | query | `string` | no |
| `orderId` | query | `string` | no |
| `q` | query | `string` | no |
| `sortBy` | query | `string` | no |
