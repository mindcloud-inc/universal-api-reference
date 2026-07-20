# urlscan.io: List Available Brands



```
GET https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/list-available-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/list-available-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/list-available-brands?${params}`, {
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
      "kits": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `kits` | array<object> |  |

## Native endpoint

Through the native urlscan.io API, this operation is `GET /api/v1/pro/availableBrands` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-brands.md) for the provider-specific parameters and requirements.

