# Update Project with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2.0/companies({{companyId}})/projects(:projectId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `list` | no |
| `sellToCustomerNo` | body | `string` | no |
| `projectId` | path | `string` | no |
| `Status` | body | `string` | no |
