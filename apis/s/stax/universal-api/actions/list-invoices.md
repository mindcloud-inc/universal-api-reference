# Stax: List Invoices

Retrieves invoices from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceDue": 1,
      "createdAt": "string",
      "customerId": "string",
      "dueAt": "string",
      "id": "string",
      "status": "string",
      "total": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceDue` | number | Outstanding invoice balance. |
| `createdAt` | string | Creation timestamp. |
| `customerId` | string | Associated customer identifier. |
| `dueAt` | string | Invoice due timestamp. |
| `id` | string | Stax invoice identifier. |
| `status` | string | Invoice status. |
| `total` | number | Invoice total amount. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `GET /invoice` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

