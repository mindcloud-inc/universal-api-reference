# Resend Payments with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/process/resend`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Resend Payments](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentId` | body | `string` | yes | Unique paymentId Format: `uuid`. |
