# Enrich.so: Get Transaction History

Retrieves credit transaction history from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-transaction-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-transaction-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-transaction-history?${params}`, {
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
| `type` | string | no | Optional transaction type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Credit amount changed by the transaction. |
| `createdAt` | date | Transaction creation timestamp. |
| `description` | string | Transaction description. |
| `id` | string | Transaction identifier. |
| `type` | string | Transaction type. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /wallets/transactions` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-transaction-history.md) for the provider-specific parameters and requirements.

