# Wikipedia: Get Page Extract

Retrieves a page extract from Wikipedia.

```
GET https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/get-page-extract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikipedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/get-page-extract?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/get-page-extract?${params}`, {
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
      "batchcomplete": true,
      "continue": {},
      "query": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchcomplete` | boolean | Indicates whether the response finished without a continuation token. |
| `continue` | object | Continuation values to request the next page of results. |
| `query` | object | Wikipedia query payload containing the requested results. |

## Native endpoint

Through the native Wikipedia API, this operation is `GET /w/api.php?action=query&prop=extracts&explaintext=1&format=json&formatversion=2&redirects=1` (base URL `https://en.wikipedia.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-extract.md) for the provider-specific parameters and requirements.

