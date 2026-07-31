# Chuck Norris: Search Facts



```
GET https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/search-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chuck Norris `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/search-facts?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chuckNorris/latest/actions/search-facts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Free-text search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> | Matching fact objects. |
| `total` | number | Total matching facts. |

## Native endpoint

Through the native Chuck Norris API, this operation is `GET /jokes/search` (base URL `https://api.chucknorris.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-facts.md) for the provider-specific parameters and requirements.

