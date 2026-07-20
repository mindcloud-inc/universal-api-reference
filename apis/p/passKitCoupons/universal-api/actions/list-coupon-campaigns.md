# PassKit Coupons: List Coupon Campaigns



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/list-coupon-campaigns?${params}`, {
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
      "error": {
        "code": 1,
        "message": "string"
      },
      "result": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `result.created` | date |  |
| `result.ianaTimezone` | string |  |
| `result.id` | string |  |
| `result.name` | string |  |
| `result.passTypeIdentifier` | string |  |
| `result.status[]` | string |  |
| `result.updated` | date |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `POST /coupon/singleUse/campaigns/list` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupon-campaigns.md) for the provider-specific parameters and requirements.

