# Get Aged Transactions with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/v2.0/companies(:companyID)/atsagedAccountsReceivables`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyID` | path | `string` | no |
| `$filter` | query | `string` | no |
