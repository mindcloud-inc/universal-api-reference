# Create Payment Approval with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/approval`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Approval](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `approvallevel` | body | `list<string>` | yes | Accepted values: `AllPayments`, `None`. |
