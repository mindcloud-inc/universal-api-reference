# Create Payment Tenant Provider Configuration with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/configuration/tenant/provider`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Tenant Provider Configuration](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `paymentProviderId` | body | `number` | yes | Payment provider (0 = Unknown, 1 = Finexio) |
| `configuration` | body | `object` | yes | Payment provider configuration |
| `configuration.url` | body | `string` | yes | Service URL |
| `configuration.username` | body | `string` | yes | Username for Finexio API |
| `configuration.password` | body | `string` | no | Sensitive value. Password for Finexio API |
