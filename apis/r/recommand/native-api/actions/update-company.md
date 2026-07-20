# Update Company with Recommand

Updates an existing company in Recommand.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/companies/:companyId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Update Company](https://recommand.eu/en/reference/companies/update-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | address body field. |
| `city` | body | `string` | no | city body field. |
| `companyId` | path | `string` | yes | companyId parameter. |
| `country` | body | `string` | no | country body field. |
| `email` | body | `string` | no | email body field. |
| `enterpriseNumber` | body | `string` | no | enterpriseNumber body field. |
| `enterpriseNumberScheme` | body | `string` | no | enterpriseNumberScheme body field. |
| `isSmpRecipient` | body | `boolean` | no | isSmpRecipient body field. |
| `name` | body | `string` | no | name body field. |
| `phone` | body | `string` | no | phone body field. |
| `postalCode` | body | `string` | no | postalCode body field. |
| `vatNumber` | body | `string` | no | vatNumber body field. |
