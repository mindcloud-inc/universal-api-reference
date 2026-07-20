# Trove: Enrich Sample Transaction

Retrieves enrichment details for a sample transaction from Trove.

```
GET https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trove/latest/actions/enrich-sample-transaction?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Trove API returns.

## Native endpoint

Through the native Trove API, this operation is `POST /transactions/enrich` (base URL `https://trove.headline.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-sample-transaction.md) for the provider-specific parameters and requirements.

