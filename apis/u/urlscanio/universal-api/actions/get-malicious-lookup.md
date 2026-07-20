# urlscan.io: Get Malicious Lookup



```
GET https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-malicious-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-malicious-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-malicious-lookup?${params}`, {
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
      "count": 1,
      "firstSeen": "string",
      "lastSeen": "string",
      "observable": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `firstSeen` | string |  |
| `lastSeen` | string |  |
| `observable` | string |  |
| `type` | string |  |

## Native endpoint

Through the native urlscan.io API, this operation is `GET /api/v1/malicious/{type}/{value}` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-malicious-lookup.md) for the provider-specific parameters and requirements.

