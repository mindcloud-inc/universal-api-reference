# Builder.io: List Models

Retrieves content models from Builder.io Admin API.

```
GET https://connect.mindcloud.co/v1/universal/builderio/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Builder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/builderio/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/builderio/latest/actions/list-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Builder.io API returns.

## Native endpoint

Through the native Builder.io API, this operation is `POST api/v2/admin` (base URL `https://cdn.builder.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

