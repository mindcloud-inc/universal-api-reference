# BuildChatbot: Get Coupon Discount Percent

Retrieves a coupon discount percent from BuildChatbot.

```
GET https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-coupon-discount-percent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-coupon-discount-percent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-coupon-discount-percent?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Coupon discount details. |
| `status` | string | Provider response status. |

## Native endpoint

Through the native BuildChatbot API, this operation is `GET /checkout/get/coupon/discount_percent/` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-discount-percent.md) for the provider-specific parameters and requirements.

