# Owen Wilson Wow API: List Wow Movies



```
GET https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/list-wow-movies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Owen Wilson Wow API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/list-wow-movies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/owenWilsonWowAPI/latest/actions/list-wow-movies?${params}`, {
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
    {}
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<string> | Movie titles containing a wow. |

## Native endpoint

Through the native Owen Wilson Wow API API, this operation is `GET /wows/movies` (base URL `https://owen-wilson-wow-api.onrender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-wow-movies.md) for the provider-specific parameters and requirements.

