# JotUrl: Get Last URL

Retrieves recent tracking links from JotUrl.

```
GET https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-last-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JotUrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-last-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-last-url?${params}`, {
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
      "creation": "string",
      "id": "string",
      "short_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creation` | string |  |
| `id` | string |  |
| `short_url` | string |  |

## Native endpoint

Through the native JotUrl API, this operation is `GET /urls/last` (base URL `https://joturl.com/a/i1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-url.md) for the provider-specific parameters and requirements.

