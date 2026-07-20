# Delete Invoice Queue Record with Rillion Prime

## Endpoint

- **Method:** `DELETE`
- **Path:** `/invoicequeue/:invoiceQueueId/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Delete Invoice Queue Record](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceQueueId` | path | `number` | yes | Path value for InvoiceQueueId. |
| `role` | path | `string` | yes | Path value for Role. |
| `deleteImages` | query | `boolean` | no | Optional query value for DeleteImages. |
