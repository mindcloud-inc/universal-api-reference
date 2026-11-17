# Create Ship-To Addresses ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/shipToAddresses`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Customer_No` | body | `string` | no |
| `Code` | body | `string` | no |
| `Name` | body | `string` | no |
| `Address` | body | `string` | no |
| `Address_2` | body | `string` | no |
| `Post_Code` | body | `string` | no |
| `City` | body | `string` | no |
| `Country_Region_Code` | body | `string` | no |
| `Phone_No` | body | `string` | no |
| `company` | path | `list` | no |
| `Contact` | body | `string` | no |
| `Salesperson_Code` | body | `string` | no |
| `Location_Code` | body | `string` | no |
| `Tax_Area_Code` | body | `string` | no |
