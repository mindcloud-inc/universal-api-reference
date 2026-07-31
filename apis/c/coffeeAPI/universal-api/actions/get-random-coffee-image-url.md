# Coffee API: Get Random Coffee Image URL



```
GET https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coffee API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coffeeAPI/latest/actions/get-random-coffee-image-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Provider-hosted URL of a random coffee image. |

## Native endpoint

Through the native Coffee API API, this operation is `GET /random.json` (base URL `https://coffee.alexflipnote.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-coffee-image-url.md) for the provider-specific parameters and requirements.

