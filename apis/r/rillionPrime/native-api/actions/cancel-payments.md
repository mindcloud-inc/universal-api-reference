# Cancel Payments with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/process/cancel`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Cancel Payments](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentIds[]` | body | `array<string>` | yes | — |
| `paymentCancellationReason` | body | `list<string>` | yes | Reason for payment cancellation Accepted values: `HandledExternally`, `SendBack`, `Voided`. |
