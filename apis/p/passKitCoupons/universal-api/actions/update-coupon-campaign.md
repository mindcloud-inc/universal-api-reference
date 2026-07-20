# PassKit Coupons: Update Coupon Campaign



```
PUT https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/update-coupon-campaign', {
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
      "created": "2026-05-07T12:00:00.000Z",
      "ianaTimezone": "string",
      "id": "string",
      "name": "Ava Chen",
      "passTypeIdentifier": "string",
      "status": [
        "string"
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `ianaTimezone` | string |  |
| `id` | string |  |
| `name` | string |  |
| `passTypeIdentifier` | string |  |
| `status[]` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `PUT /coupon/singleUse/campaign` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon-campaign.md) for the provider-specific parameters and requirements.

