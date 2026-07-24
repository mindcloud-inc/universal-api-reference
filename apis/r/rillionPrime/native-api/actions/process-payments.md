# Process Payments with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/process`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Process Payments](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentIds[]` | body | `array<string>` | yes | — |
| `setScheduledDate` | body | `date` | no | Scheduled date to apply to the payment. Only allowed when paymentStatus is PaymentAwaitingApproval or PaymentApproved. Time of day comes from the schedule. Format: `date`. |
| `removeScheduledDate` | body | `boolean` | no | Set to true to remove the scheduled date and recompute it from the schedule settings. Only allowed when paymentStatus is PaymentCreated. |
