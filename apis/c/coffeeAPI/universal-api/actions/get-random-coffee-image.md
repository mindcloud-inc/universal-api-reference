# Coffee API: Get Random Coffee Image



```
GET https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coffee API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coffee API API returns.

## Native endpoint

Through the native Coffee API API, this operation is `GET /random` (base URL `https://coffee.alexflipnote.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-coffee-image.md) for the provider-specific parameters and requirements.

