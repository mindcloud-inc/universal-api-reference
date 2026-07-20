# Manage Bookings with KleverKey

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/organizations/:organizationId/bookings/:serviceName`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Manage Bookings](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | — |
| `serviceName` | path | `string` | yes | — |
| `operationType` | body | `number` | yes | 1 = CreateOrUpdate, 2 = Delete |
| `userEmail` | body | `string` | no | Email for the booking user. |
| `userName` | body | `string` | no | Display name for the booking user. |
| `permission.lockIds` | body | `string` | yes | Comma separated list of lock IDs |
| `permission.referenceId` | body | `string` | yes | — |
