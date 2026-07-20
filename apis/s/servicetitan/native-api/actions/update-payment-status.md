# Update Payment Status with ServiceTitan

Updates a payment status in ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/payments/status`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `paymentIds[]` | body | `array<string>` | no |
| `status` | body | `string` | no |
