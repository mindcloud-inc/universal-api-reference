# Wisewand: List transactions

Retrieves transactions from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/list-transactions?${params}`, {
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
| `start_date` | string | no | ISO 8601 format |
| `end_date` | string | no | ISO 8601 format |
| `reason` | string | no | Filter by reason(s). Can be a single value or multiple values separated by commas (e.g., "payment,task_run") |
| `debits_only` | boolean | no | Filter to show only debit transactions (negative credits) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `items` | array<object> |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/transactions/` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

