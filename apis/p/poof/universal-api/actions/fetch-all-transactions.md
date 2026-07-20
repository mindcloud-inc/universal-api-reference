# Poof: Fetch All Transactions

Retrieves all transaction records from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-all-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-all-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-all-transactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Poof API returns.

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v1/fetch_transactions` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-all-transactions.md) for the provider-specific parameters and requirements.

