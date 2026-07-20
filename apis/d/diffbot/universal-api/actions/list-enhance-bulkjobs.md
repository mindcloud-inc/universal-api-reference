# Diffbot: List Enhance Bulkjobs

Lists Enhance bulk jobs for the current Diffbot token.

```
GET https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/list-enhance-bulkjobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/list-enhance-bulkjobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffbot/latest/actions/list-enhance-bulkjobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Diffbot API returns.

## Native endpoint

Through the native Diffbot API, this operation is `GET https://kg.diffbot.com/kg/v3/enhance/bulk/status` (base URL `https://api.diffbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-enhance-bulkjobs.md) for the provider-specific parameters and requirements.

