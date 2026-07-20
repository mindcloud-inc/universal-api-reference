# Rillion Prime: List Invoice Account Coding Posts Batch



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-account-coding-posts-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-account-coding-posts-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-account-coding-posts-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceIds` | array | no | Request body value for InvoiceIds. |
| `pageIndex` | number | no | Request body value for PageIndex. |
| `pageSize` | number | no | Request body value for PageSize. |
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceIds` | array | no | Request body value for InvoiceIds. |
| `pageIndex` | number | no | Request body value for PageIndex. |
| `pageSize` | number | no | Request body value for PageSize. |
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceIds` | array | no | Request body value for InvoiceIds. |
| `pageIndex` | number | no | Request body value for PageIndex. |
| `pageSize` | number | no | Request body value for PageSize. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/accountcoding` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-account-coding-posts-batch.md) for the provider-specific parameters and requirements.

