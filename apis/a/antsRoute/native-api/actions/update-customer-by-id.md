# Update Customer by ID with AntsRoute

Updates an existing customer in AntsRoute by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/capi/customer/id/:id`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Update Customer by ID](https://app.antsroute.com/doc-api/index.html#/Customer/updateCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Address of the customer |
| `comments` | body | `string` | no | Customer comments. |
| `email` | body | `string` | no | Customer email address. |
| `externalId` | body | `string` | no | External customer ID. |
| `firstName` | body | `string` | no | First name of the customer |
| `id` | path | `number` | yes | Customer ID |
| `lastName` | body | `string` | yes | Last name of the customer |
| `latitude` | body | `number` | yes | Customer latitude. |
| `longitude` | body | `number` | yes | Customer longitude. |
| `mobileNumber` | body | `string` | no | Customer mobile number. |
| `openingHoursAlwaysOpen` | body | `boolean` | no | Whether the customer is always open. |
| `parkingTimeInMinutes` | body | `number` | no | Parking time in minutes. |
| `phoneNumber` | body | `string` | no | Customer phone number. |
| `skills[]` | body | `array<string>` | no | Required customer skills. |
