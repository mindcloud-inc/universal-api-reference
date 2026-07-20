# Rillion Prime: Delete Invoice Queue Record



```
DELETE https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-queue-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-queue-record?connectionId=$CONNECTION_ID&invoiceQueueId=1&role=Administrator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceQueueId": "1",
  "role": "Administrator"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-queue-record?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceQueueId` | number | yes | Path value for InvoiceQueueId. |
| `role` | string | yes | Path value for Role. Example: `Administrator`. |
| `deleteImages` | boolean | no | Optional query value for DeleteImages. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `DELETE /invoicequeue/:invoiceQueueId/role/:role` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice-queue-record.md) for the provider-specific parameters and requirements.

