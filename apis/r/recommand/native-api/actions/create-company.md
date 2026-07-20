# Create Company with Recommand

Creates a new company in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/companies`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Company](https://recommand.eu/en/reference/companies/create-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | address body field. |
| `city` | body | `string` | yes | city body field. |
| `country` | body | `string` | yes | country body field. |
| `email` | body | `string` | no | email body field. |
| `enterpriseNumber` | body | `string` | no | The enterprise number of the company. Can only contain alphanumeric characters. For Belgian businesses it will be inferred from the VAT number if not provided. |
| `enterpriseNumberScheme` | body | `string` | no | enterpriseNumberScheme body field. |
| `isSmpRecipient` | body | `boolean` | no | isSmpRecipient body field. |
| `name` | body | `string` | yes | name body field. |
| `phone` | body | `string` | no | phone body field. |
| `postalCode` | body | `string` | yes | postalCode body field. |
| `skipDefaultCompanySetup` | body | `boolean` | no | If true, the automatic creation of company identifiers and document types will be skipped. You will need to create them afterwards using the company identifier creation endpoint and company document type creation endpoint. |
| `vatNumber` | body | `string` | no | vatNumber body field. |
