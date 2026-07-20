# TemplateFox: List Transactions

Retrieves account transactions from TemplateFox.

```
GET https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TemplateFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/list-transactions?${params}`, {
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
| `limit` | number | no | Number of transactions to return. Example: `300`. |
| `offset` | number | no | Number of transactions to skip. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits": 1,
      "exec_tm": 1,
      "template_id": "string",
      "transaction_ref": "string",
      "transaction_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `credits` | number |  |
| `exec_tm` | number |  |
| `template_id` | string |  |
| `transaction_ref` | string |  |
| `transaction_type` | string |  |

## Native endpoint

Through the native TemplateFox API, this operation is `GET /v1/account/transactions` (base URL `https://api.templatefox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

