# Update Payment with ServiceTitan

Updates an existing payment in ServiceTitan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounting/v2/tenant/{tenant}/payments/{{paymentId}}`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | body | `string` | no |
| `typeId` | body | `string` | no |
| `amount` | body | `string` | no |
| `date` | body | `string` | no |
| `checkNumber` | body | `string` | no |
| `referenceNumber` | body | `string` | no |
| `memo` | body | `string` | no |
| `syncStatus` | body | `string` | no |
| `paymentId` | path | `number` | no |
| `splits[]` | body | `array<object>` | no |
