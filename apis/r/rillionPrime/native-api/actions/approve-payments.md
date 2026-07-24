# Approve Payments with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/process/approve`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Approve Payments](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentIds[]` | body | `array<string>` | yes | — |
| `processInstantly` | body | `boolean` | no | If true, payments will be processed instantly after approval |
| `processAccordingToSchedule` | body | `boolean` | no | If true, payments will be processed on the next scheduled date after approval |
