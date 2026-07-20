# PassKit Coupons: Get Coupon Campaign



```
GET https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Coupons `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitCoupons/latest/actions/get-coupon-campaign?${params}`, {
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
| `id` | string | yes | Coupon campaign ID. |

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

Through the native PassKit Coupons API, this operation is `GET /coupon/singleUse/campaign/:id` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon-campaign.md) for the provider-specific parameters and requirements.

