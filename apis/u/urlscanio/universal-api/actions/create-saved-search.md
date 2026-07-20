# urlscan.io: Create Saved Search



```
POST https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/create-saved-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/create-saved-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/create-saved-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "search": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `search` | object |  |

## Native endpoint

Through the native urlscan.io API, this operation is `POST /api/v1/user/searches/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-saved-search.md) for the provider-specific parameters and requirements.

