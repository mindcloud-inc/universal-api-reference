# Create Company Identifier with Recommand

Creates a new company identifier in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/companies/:companyId/identifiers`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Company Identifier](https://recommand.eu/en/reference/company-identifiers/create-company-identifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `identifier` | body | `string` | yes | The value of the identifier |
| `scheme` | body | `string` | yes | The scheme of the identifier |
