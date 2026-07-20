# Update Customer with GatherUp

Updates an existing customer in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/update`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update Customer](https://app.gatherup.com/api/doc/customer/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerEmail` | body | `string` | no | Customer email address. |
| `customerFirstName` | body | `string` | no | Customer first name. |
| `customerId` | body | `number` | yes | Customer id. |
| `customerLastName` | body | `string` | no | Customer last name. |
| `customerPhoneNumber` | body | `string` | no | Customer mobile phone number. |
| `customerPreference` | body | `string` | no | Customer communication preference. |
| `customerCustomId` | body | `number` | no | Customer custom id. |
| `customerJobId` | body | `number` | no | Customer job id. |
| `customerTags` | body | `string` | no | Overwrites / Removes existing Customer tags with the new tags specified. Add tags comma separated. |
