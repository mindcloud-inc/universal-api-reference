# Stax: List Transactions

Retrieves transactions from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-transactions?${params}`, {
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
| `direction` | string | no | Sort direction. |
| `page` | string | no | Page number for paginated transaction results. |
| `sort` | string | no | Transaction sort field. |
| `status` | string | no | Transaction status selector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customerId": "string",
      "id": "string",
      "status": "string",
      "total": 1,
      "transactionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `customerId` | string | Associated customer identifier. |
| `id` | string | Stax transaction identifier. |
| `status` | string | Transaction status. |
| `total` | number | Transaction total amount. |
| `transactionType` | string | Transaction type. |

## Native endpoint

Through the native Stax API, this operation is `GET /transaction` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

