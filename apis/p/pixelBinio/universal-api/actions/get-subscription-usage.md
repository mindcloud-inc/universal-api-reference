# PixelBin.io: Get Subscription Usage

Retrieves subscription usage details from PixelBin.io.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-subscription-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-subscription-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-subscription-usage?${params}`, {
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
      "credits": {},
      "total": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | object | Current credit usage values. |
| `total` | object | Subscription total allotments. |
| `usage` | object | Current subscription usage values. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/payment/v1.0/usage/subscription` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-usage.md) for the provider-specific parameters and requirements.

