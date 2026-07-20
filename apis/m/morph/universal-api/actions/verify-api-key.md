# Morph: Verify API Key

Verifies a Morph API key with a fixed embedding request.

```
GET https://connect.mindcloud.co/v1/universal/morph/latest/actions/verify-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morph/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morph/latest/actions/verify-api-key?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morph API returns.

## Native endpoint

Through the native Morph API, this operation is `POST /embeddings` (base URL `https://api.morphllm.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-key.md) for the provider-specific parameters and requirements.

