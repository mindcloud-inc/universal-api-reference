# Create Payment Tenant Configuration with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/configuration/tenant`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Tenant Configuration](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentProviderId` | body | `number` | yes | Payment provider (0 = Unknown, 1 = Finexio) |
