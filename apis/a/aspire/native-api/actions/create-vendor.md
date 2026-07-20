# Create Vendor with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `Vendors`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Vendor](https://guide.youraspire.com/apidocs/vendors-3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `BranchID` | body | `list<number>` | no |
| `VendorName` | body | `string` | yes |
| `AccountingVendorID` | body | `string` | no |
| `BillingTerms` | body | `string` | no |
| `Active` | body | `boolean` | yes |
