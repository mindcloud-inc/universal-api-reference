# Create Customer with AntsRoute

Creates a new customer in AntsRoute.

## Endpoint

- **Method:** `POST`
- **Path:** `/capi/customer`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Create Customer](https://app.antsroute.com/doc-api/index.html#/Customer/createCustomer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Address of the customer |
| `comments` | body | `string` | no | Customer comments. |
| `email` | body | `string` | no | Customer email address. |
| `externalId` | body | `string` | no | External customer ID. |
| `firstName` | body | `string` | no | First name of the customer |
| `lastName` | body | `string` | yes | Last name of the customer |
| `latitude` | body | `number` | yes | Location latitude of the customer |
| `longitude` | body | `number` | yes | Location longitude of the customer |
| `mobileNumber` | body | `string` | no | Customer mobile number. |
| `openingHoursAlwaysOpen` | body | `boolean` | no | Whether the customer is always open. |
| `parkingTimeInMinutes` | body | `number` | no | Parking time in minutes. |
| `phoneNumber` | body | `string` | no | Customer phone number. |
| `skills[]` | body | `array<string>` | no | Required customer skills. |
