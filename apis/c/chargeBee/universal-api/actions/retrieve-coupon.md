# ChargeBee: Retrieve Coupon

Retrieves a coupon from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-coupon?connectionId=$CONNECTION_ID&coupon_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "coupon_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-coupon?${params}`, {
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
| `coupon_id` | string | yes | The Chargebee coupon identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "discount_type": "string",
      "duration_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "status": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `discount_type` | string |  |
| `duration_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `status` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET coupons/:coupon_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-coupon.md) for the provider-specific parameters and requirements.

