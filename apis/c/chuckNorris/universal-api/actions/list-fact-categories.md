# Chuck Norris: List Fact Categories



```
GET https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/list-fact-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chuck Norris `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/list-fact-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/list-fact-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chuck Norris API returns.

## Native endpoint

Through the native Chuck Norris API, this operation is `GET /jokes/categories` (base URL `https://api.chucknorris.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fact-categories.md) for the provider-specific parameters and requirements.

