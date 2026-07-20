# Rillion Prime: Delete Invoice Account Coding Queue



```
DELETE https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-account-coding-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-account-coding-queue?connectionId=$CONNECTION_ID&invoiceAccountCodingQueueId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceAccountCodingQueueId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/delete-invoice-account-coding-queue?${params}`, {
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
| `invoiceAccountCodingQueueId` | number | yes | Path value for InvoiceAccountCodingQueueId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `DELETE /invoiceaccountcodingqueue/:invoiceaccountcodingqueueid` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice-account-coding-queue.md) for the provider-specific parameters and requirements.

