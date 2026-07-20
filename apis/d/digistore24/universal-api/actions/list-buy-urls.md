# Digistore24: List Buy URLs

Retrieves a list of buy URLs from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-buy-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-buy-urls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-buy-urls?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "productId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `id` | number | Buy URL ID |
| `modifiedAt` | date | Last modification timestamp |
| `productId` | number | Product ID |
| `url` | string | Buy URL |

## Native endpoint

Through the native Digistore24 API, this operation is `GET /listBuyUrls` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buy-urls.md) for the provider-specific parameters and requirements.

