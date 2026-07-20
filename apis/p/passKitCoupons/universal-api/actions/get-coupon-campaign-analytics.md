# PassKit Coupons: Get Coupon Campaign Analytics



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign-analytics?connectionId=$CONNECTION_ID&classId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign-analytics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classId` | string | yes | Coupon campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created": 1,
          "custom": 1,
          "deleted": 1,
          "installed": 1,
          "invalidated": 1,
          "name": "Ava Chen",
          "updated": 1
        }
      ],
      "devices": {
        "appleWallet": 1,
        "googlePay": 1,
        "otherWallet": 1
      },
      "period": "string",
      "redeemed": 1,
      "sources": {
        "*": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created` | number |  |
| `data[].custom` | number |  |
| `data[].deleted` | number |  |
| `data[].installed` | number |  |
| `data[].invalidated` | number |  |
| `data[].name` | string |  |
| `data[].updated` | number |  |
| `devices.appleWallet` | number |  |
| `devices.googlePay` | number |  |
| `devices.otherWallet` | number |  |
| `period` | string |  |
| `redeemed` | number |  |
| `sources.*` | number |  |

## Native endpoint

Through the native PassKit Coupons API, this operation is `GET /coupon/singleUse/campaign/:classId/analytics` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-campaign-analytics.md) for the provider-specific parameters and requirements.

