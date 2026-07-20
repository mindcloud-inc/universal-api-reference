# Becon: Get Transaction

Retrieves a transaction from Becon by ID.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-transaction?connectionId=$CONNECTION_ID&txid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "txid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/get-transaction?${params}`, {
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
| `txid` | string | yes | Blockchain transaction id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "created_at": "string",
      "id": 1,
      "log_line": "string",
      "status": "string",
      "sum": "string",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Receiving address. |
| `created_at` | string | Transaction creation timestamp. |
| `id` | number | Internal transaction id. |
| `log_line` | string | Callback log line URL. |
| `status` | string | Transaction confirmation status. |
| `sum` | string | Transferred amount. |
| `transaction_id` | string | Blockchain transaction id. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/transactions/:txid` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

