# Poof: Transaction Query

Retrieves transaction query results from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/transaction-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/transaction-query?connectionId=$CONNECTION_ID&filter=payment&search=usdc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "payment",
  "search": "usdc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/transaction-query?${params}`, {
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
| `filter` | string | yes | Transaction query filter key. Default: `payment`. |
| `search` | string | yes | Transaction query search value. Default: `usdc`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Poof API returns.

## Native endpoint

Through the native Poof API, this operation is `POST /transaction_query` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transaction-query.md) for the provider-specific parameters and requirements.

