# Update Company with OneSuite

Updates a company in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/companies/:company_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Company](https://rest-api.onesuite.io/#update-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Company ID from the OneSuite update-company docs. |
| `name` | body | `string` | no | Updated company name. |
