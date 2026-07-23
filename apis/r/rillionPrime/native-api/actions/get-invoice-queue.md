# Get Invoice Queue with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/invoicequeue/:invoiceQueueId/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Invoice Queue](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceQueueId` | path | `number` | yes | Path value for InvoiceQueueId. |
| `role` | path | `string` | yes | Path value for Role. |
| `headersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
