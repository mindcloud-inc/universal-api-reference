# Rillion Prime: Get Invoice Details



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-invoice-details?connectionId=$CONNECTION_ID&environment=string&user=AdminUser&role=Administrator&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environment": "string",
  "user": "AdminUser",
  "role": "Administrator",
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/get-invoice-details?${params}`, {
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
| `environment` | string | yes | Optional query value for Environment. |
| `user` | string | yes | Optional query value for User. Example: `AdminUser`. |
| `role` | string | yes | Optional query value for Role. Example: `Administrator`. |
| `invoiceId` | number | yes | Optional query value for InvoiceId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `GET /invoice/detail` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-details.md) for the provider-specific parameters and requirements.

