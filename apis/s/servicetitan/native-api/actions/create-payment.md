# Create Payment with ServiceTitan

Creates a new payment in ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/payments`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `string` | no | — |
| `paymentTypeId` | body | `string` | no | — |
| `amount` | body | `string` | no | — |
| `date` | body | `string` | no | — |
| `checkNumber` | body | `string` | no | — |
| `referenceNumber` | body | `string` | no | — |
| `memo` | body | `string` | no | — |
| `syncStatus` | body | `string` | no | — |
| `customFields[]` | body | `array<object>` | no | ServiceTitan payment custom fields. Use VistaID type 13614166 to store the Vista receipt identifier. |
