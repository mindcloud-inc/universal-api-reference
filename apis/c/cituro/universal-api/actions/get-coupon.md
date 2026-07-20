# Cituro: Get Coupon

Retrieves a coupon record from Cituro.

```
GET https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cituro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-coupon?connectionId=$CONNECTION_ID&couponId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "couponId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-coupon?${params}`, {
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
| `couponId` | string | yes | Cituro coupon identifier from the coupon resource path. |

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
| `id` | string | Unique Cituro coupon identifier. |

## Native endpoint

Through the native Cituro API, this operation is `GET /coupons/:couponId` (base URL `https://app.cituro.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon.md) for the provider-specific parameters and requirements.

