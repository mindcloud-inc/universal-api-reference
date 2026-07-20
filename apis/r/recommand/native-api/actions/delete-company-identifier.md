# Delete Company Identifier with Recommand

Deletes a company identifier from Recommand.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/companies/:companyId/identifiers/:identifierId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Delete Company Identifier](https://recommand.eu/en/reference/company-identifiers/delete-company-identifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `identifierId` | path | `string` | yes | identifierId parameter. |
