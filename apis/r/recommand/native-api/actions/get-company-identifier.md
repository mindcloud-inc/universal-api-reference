# Get Company Identifier with Recommand

Retrieves a company identifier from Recommand.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/companies/:companyId/identifiers/:identifierId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Get Company Identifier](https://recommand.eu/en/reference/company-identifiers/get-company-identifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `identifierId` | path | `string` | yes | identifierId parameter. |
