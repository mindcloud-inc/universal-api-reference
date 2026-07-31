# PoetryDB: List Authors



```
GET https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/list-authors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PoetryDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/list-authors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poetryDB/latest/actions/list-authors?${params}`, {
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
      "authors": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<string> |  |

## Native endpoint

Through the native PoetryDB API, this operation is `GET /author` (base URL `https://poetrydb.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-authors.md) for the provider-specific parameters and requirements.

