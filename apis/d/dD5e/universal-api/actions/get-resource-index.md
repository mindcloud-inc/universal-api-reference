# D&D 5e: Get Resource Index



```
GET https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-resource-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D&D 5e `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-resource-index?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-resource-index?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native D&D 5e API returns.

## Native endpoint

Through the native D&D 5e API, this operation is `GET /` (base URL `https://www.dnd5eapi.co/api/2014`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-index.md) for the provider-specific parameters and requirements.

