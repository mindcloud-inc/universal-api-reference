# Rillion Prime: List Invoice Diary Posts



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-diary-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-diary-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-invoice-diary-posts?${params}`, {
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
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceId` | number | no | Request body value for InvoiceId. |
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceId` | number | no | Request body value for InvoiceId. |
| `environment` | string | no | Request body value for Environment. |
| `user` | string | no | Request body value for User. Example: `AdminUser`. |
| `role` | string | no | Request body value for Role. Example: `Administrator`. |
| `invoiceId` | number | no | Request body value for InvoiceId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /invoice/diary` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-diary-posts.md) for the provider-specific parameters and requirements.

