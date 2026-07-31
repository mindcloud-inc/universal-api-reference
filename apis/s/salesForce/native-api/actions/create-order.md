# Create Order with Salesforce

## Endpoint

- **Method:** `POST`
- **Path:** `/services/data/v64.0/sobjects/Order`
- **Base URL:** `https://{companyDomainName}.my.salesforce.com`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | yes |
| `Pricebook2Id` | body | `string` | no |
| `Status` | body | `string` | no |
| `EffectiveDate` | body | `string` | yes |
| `poNumber` | body | `string` | no |
| `shippingStreet` | body | `string` | no |
| `shippingCity` | body | `string` | no |
| `shippingState` | body | `string` | no |
| `shippingPostalCode` | body | `string` | no |
| `shippingCountry` | body | `string` | no |
