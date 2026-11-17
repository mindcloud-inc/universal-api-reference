# Update Ship-to Addresses SSI ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company_id)/shipToAddresses`
- **API:** REST (Copy)
- **Official documentation:** [Update Ship-to Addresses SSI ODataV4](https://anotepad.com/notes/x8dnaab8)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Customer_No` | body | `string` | no |
| `Name` | body | `string` | no |
| `Post_Code` | body | `string` | no |
| `company_id` | path | `list` | no |
| `Code` | body | `string` | no |
| `Address` | body | `string` | no |
| `Address_2` | body | `string` | no |
| `City` | body | `string` | no |
| `Contact` | body | `string` | no |
| `Country_Region_Code` | body | `string` | no |
| `Location_Code` | body | `string` | no |
| `Phone_No` | body | `string` | no |
| `Salesperson_Code` | body | `string` | no |
| `Tax_Area_Code` | body | `string` | no |
