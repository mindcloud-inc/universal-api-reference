# Create Booking with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v2/tenant/{tenant}/booking-provider/:bookingProviderId/bookings`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Booking](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Bookings_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.city` | body | `string` | no | — |
| `address.state` | body | `string` | no | — |
| `address.zip` | body | `string` | no | — |
| `address.street` | body | `string` | no | — |
| `contacts[].type` | body | `string` | no | Phone , Phone , Email , Fax , MobilePhone |
| `summary` | body | `string` | yes | — |
| `address.unit` | body | `string` | no | — |
| `contacts[].value` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `contacts[].memo` | body | `string` | no | — |
| `externalId` | body | `string` | yes | — |
| `isFirstTimeClient` | body | `boolean` | yes | Format: `toggle`. |
| `source` | body | `string` | yes | — |
| `address.country` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `address` | body | `object` | no | — |
| `contacts[]` | body | `array` | no | — |
| `customerType` | body | `string` | no | — |
| `start` | body | `string` | no | — |
| `priority` | body | `object` | no | — |
| `uploadedImages` | body | `array` | no | — |
| `isSendConfirmationEmail` | body | `boolean` | no | — |
| `bookingProviderId` | path | `list` | no | — |
