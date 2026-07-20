# Recut URL Shortener: List QR Codes

Retrieves QR codes from Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-qr-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-qr-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-qr-codes?${params}`, {
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
      "data": {},
      "error": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | number |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /qr` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-qr-codes.md) for the provider-specific parameters and requirements.

