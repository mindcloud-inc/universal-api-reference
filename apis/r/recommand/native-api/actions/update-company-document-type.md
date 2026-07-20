# Update Company Document Type with Recommand

Updates an existing company document type in Recommand.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/companies/:companyId/document-types/:documentTypeId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Update Company Document Type](https://recommand.eu/en/reference/company-document-types/update-company-document-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `docTypeId` | body | `string` | yes | The ID of the document type to update |
| `documentTypeId` | path | `string` | yes | documentTypeId parameter. |
| `processId` | body | `string` | yes | The ID of the process to update |
