# List Company People with OneSuite

Retrieves a company's people from OneSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/:company_id/people`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [List Company People](https://rest-api.onesuite.io/#get-company-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Company ID from the OneSuite company-people docs. |
