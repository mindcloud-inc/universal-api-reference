# Create Payment with PestPac

## Endpoint

- **Method:** `POST`
- **Path:** `Payments`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `string` | yes |
| `billToID` | body | `string` | no |
| `methodOfPayment` | body | `string` | no |
| `paymentDate` | body | `string` | yes |
| `paymentType` | body | `string` | yes |
| `applications[]` | body | `array` | no |
