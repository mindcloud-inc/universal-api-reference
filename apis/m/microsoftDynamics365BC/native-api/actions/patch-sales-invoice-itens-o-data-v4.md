# Patch Sales Invoice Itens ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:company)/MindcloudSalesInvoiceSalesLines(Document_Type=':documentType',Document_No=':documentNo',Line_No=:lineNo)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company` | path | `list` | no |
| `Description` | body | `string` | no |
| `documentType` | path | `string` | no |
| `documentNo` | path | `string` | no |
| `lineNo` | path | `string` | no |
