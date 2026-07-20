# Becon: List Transaction History

Retrieves BTC transaction history from Becon by address.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-transaction-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-transaction-history?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-transaction-history?${params}`, {
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
| `address` | string | yes | Whitespace-separated wallet addresses to inspect. |
| `page` | string | no | Page number for paginated transaction history. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "preset": "string",
      "status": "string",
      "sum": "string",
      "tag": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Transaction creation timestamp. |
| `preset` | string | Store preset name. |
| `status` | string | Transaction confirmation status. |
| `sum` | string | Transferred amount. |
| `tag` | string | Store tag. |
| `transaction_id` | string | Blockchain transaction id. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/user/history` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction-history.md) for the provider-specific parameters and requirements.

