# Update Company with Teamgate

Updates a company in Teamgate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/{{companyId}}`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Update Company](https://developers.teamgate.com/#39f561e7-d276-49a7-8873-1fc1a6758837)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | Company ID to update. |
| `industry` | body | `string` | no | Updated company industry name. |
| `name` | body | `string` | no | Updated company name. |
| `ownerId` | body | `string` | no | Updated owner user ID. |
| `source` | body | `string` | no | Updated company source name. |
| `starred` | body | `string` | no | Whether the company is starred. Use Teamgate values like yes or no. |
| `tags` | body | `string` | no | Updated company tags. |
