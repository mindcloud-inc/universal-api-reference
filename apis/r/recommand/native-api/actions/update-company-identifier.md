# Update Company Identifier with Recommand

Updates an existing company identifier in Recommand.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/companies/:companyId/identifiers/:identifierId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Update Company Identifier](https://recommand.eu/en/reference/company-identifiers/update-company-identifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `identifier` | body | `string` | yes | The value of the identifier |
| `identifierId` | path | `string` | yes | identifierId parameter. |
| `scheme` | body | `string` | yes | The scheme of the identifier |
