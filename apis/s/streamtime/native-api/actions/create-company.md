# Create Company with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Company](https://api.streamtime.net/v2/swagger#/Companies/createCompany)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Company name |
| `companyStatus` | body | `object` | no | Status of a company |
| `companyStatus.id` | body | `number` | no | Company status ID |
| `taxNumber` | body | `string` | yes | Tax/GST/VAT number |
| `phone1` | body | `string` | no | Primary phone number |
| `phone2` | body | `string` | no | Secondary phone number |
| `websiteAddress` | body | `string` | no | Website URL |
| `physicalAddress` | body | `object` | no | Physical address object |
| `physicalAddress.line1` | body | `string` | no | Physical address line 1 |
| `physicalAddress.line2` | body | `string` | no | Physical address line 2 |
| `physicalAddress.line3` | body | `string` | no | Physical address line 3 |
| `physicalAddress.city` | body | `string` | no | Physical address city |
| `physicalAddress.region` | body | `string` | no | Physical address region |
| `physicalAddress.countryName` | body | `string` | no | Physical address country name |
| `physicalAddress.postCode` | body | `string` | no | Physical address postal code |
| `postalAddress` | body | `object` | no | Postal address object |
| `postalAddress.line1` | body | `string` | no | Postal address line 1 |
| `postalAddress.line2` | body | `string` | no | Postal address line 2 |
| `postalAddress.line3` | body | `string` | no | Postal address line 3 |
| `postalAddress.city` | body | `string` | no | Postal address city |
| `postalAddress.region` | body | `string` | no | Postal address region |
| `postalAddress.countryName` | body | `string` | no | Postal address country name |
| `postalAddress.postCode` | body | `string` | no | Postal address postal code |
