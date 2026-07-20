# GoAffPro: List Coupon Codes

Retrieves assigned coupon codes from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-coupon-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-coupon-codes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-coupon-codes?${params}`, {
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
| `affiliateId` | string | no | Only return coupon codes for this affiliate ID. |
| `code` | string | no | Only return coupon codes matching this code. |
| `type` | string | no | Only return coupon codes with this type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "code": "string",
      "discountType": "string",
      "discountValue": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `code` | string |  |
| `discountType` | string |  |
| `discountValue` | number |  |
| `type` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/coupons` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupon-codes.md) for the provider-specific parameters and requirements.

