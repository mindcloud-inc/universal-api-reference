# Qdrant: List Collections

Retrieves all existing collections from Qdrant.

```
GET https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qdrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qdrant/latest/actions/list-collections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Qdrant API returns.

## Native endpoint

Through the native Qdrant API, this operation is `GET /collections` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

