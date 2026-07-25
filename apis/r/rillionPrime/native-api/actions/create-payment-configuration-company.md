# Create Payment Configuration Company with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/configuration/company`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Configuration Company](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `companyId` | body | `string` | yes | Id for the company (from Prime) |
| `companyName` | body | `string` | yes | Name for the company (from Prime) |
