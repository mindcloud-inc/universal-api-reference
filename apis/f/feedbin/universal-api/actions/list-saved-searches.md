# Feedbin: List Saved Searches

Retrieves a list of saved searches from Feedbin.

```
GET https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-saved-searches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-saved-searches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-saved-searches?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `query` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `GET saved_searches.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saved-searches.md) for the provider-specific parameters and requirements.

