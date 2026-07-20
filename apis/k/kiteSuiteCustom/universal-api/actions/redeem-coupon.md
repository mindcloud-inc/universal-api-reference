# Kite Suite: Redeem Coupon



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/redeem-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/redeem-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "code": "string",
  "element": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/redeem-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "code": "string",
    "element": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `code` | string | yes | Coupon code to redeem. |
| `element` | string | yes | ID of the form element. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "applyTo": "string",
      "code": "string",
      "couponLimit": "string",
      "discountAmt": 1,
      "discountRate": 1,
      "element": "string",
      "isEnable": true,
      "limitDate": "string",
      "limitValue": 1,
      "name": "Ava Chen",
      "totalUssage": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Coupon ID. |
| `applyTo` | string | Specifies if the coupon applies to all products or specific products. |
| `code` | string | Coupon code. |
| `couponLimit` | string | Limit type for the coupon. |
| `discountAmt` | number | Discount amount (fixed). |
| `discountRate` | number | Discount rate (percentage). |
| `element` | string | ID of the associated form element. |
| `isEnable` | boolean | Indicates if the coupon is enabled. |
| `limitDate` | string | Date and time limit for the coupon. |
| `limitValue` | number | Maximum number of times the coupon can be used. |
| `name` | string | Coupon name. |
| `totalUssage` | array<string> | array of user id that used the coupon. |
| `type` | string | Type of discount. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/form/coupon/redeem` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeem-coupon.md) for the provider-specific parameters and requirements.

