# Create Multiple Customers with GatherUp

Creates multiple new customers in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/create`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Create Multiple Customers](https://app.gatherup.com/api/doc/customers/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `customerCustomId{N}` | body | `string` | no | Customer custom id. |
| `customerEmail{N}` | body | `string` | yes | Customer email address. This field is required for basic plan accounts. For higher plans there is email or phone number required. |
| `customerFirstName{N}` | body | `string` | no | Customer first name. |
| `customerJobId{N}` | body | `string` | no | Customer job id. |
| `customerLastName{N}` | body | `string` | no | Customer last name. |
| `customerPhone{N}` | body | `string` | no | Customer phone. |
| `customerPreference{N}` | body | `string` | no | Customer communication preference. |
| `customerTags{N}` | body | `string` | no | Customer tags separated by comma (max length of one tag = 50 chars). |
