# Update Vendor with Aspire

## Endpoint

- **Method:** `PUT`
- **Path:** `Vendors`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Vendor](https://guide.youraspire.com/apidocs/vendors-12)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `BranchID` | body | `list<number>` | no |
| `VendorName` | body | `string` | yes |
| `AccountingVendorID` | body | `string` | no |
| `BillingTerms` | body | `string` | no |
| `Active` | body | `boolean` | yes |
| `VendorID` | body | `list<number>` | yes |
