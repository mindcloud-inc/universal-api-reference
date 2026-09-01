# Update Payment Custom Fields with ServiceTitan

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounting/v2/tenant/{tenant}/payments/custom-fields`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Payment Custom Fields](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/Payments_UpdateCustomFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | body | `string` | yes | — |
| `customFieldName` | body | `string` | yes | Exact name of the ServiceTitan Payment custom field. For the United Mechanical production tenant, use Vista ID. |
| `customFieldValue` | body | `string` | yes | — |
