# Update Company with folk

Updates an existing company in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/companies/:companyId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Company](https://developer.folk.app/api-reference/companies/update-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | The ID of the company to update. |
| `description` | body | `string` | no | The updated company description. |
| `name` | body | `string` | no | The updated company name. |
