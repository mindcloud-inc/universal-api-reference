# Create Company Document Type with Recommand

Creates a new company document type in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/companies/:companyId/document-types`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Company Document Type](https://recommand.eu/en/reference/company-document-types/create-company-document-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `docTypeId` | body | `string` | yes | The ID of the document type to create |
| `processId` | body | `string` | yes | The ID of the process to create |
