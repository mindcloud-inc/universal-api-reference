# Update Payment Custom Fields with ServiceTitan

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounting/v2/tenant/{tenant}/payments/custom-fields`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Payment Custom Fields](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/Payments_UpdateCustomFields)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `paymentId` | body | `string` | yes |
| `customFieldName` | body | `string` | yes |
| `customFieldValue` | body | `string` | yes |
