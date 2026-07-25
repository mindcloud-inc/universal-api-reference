# Create Payment Supplier Grouping with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/suppliers/grouping`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Supplier Grouping](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `supplierPaymentGrouping` | body | `list<string>` | yes | Payment grouping option applied to all suppliers Accepted values: `Bundle`, `SendIndividually`. |
