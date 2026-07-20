# PassKit Coupons: Update Coupon



```
PUT https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon', {
  method: 'PUT',
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `PUT /coupon/singleUse/coupon` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon.md) for the provider-specific parameters and requirements.

