# Kite Suite: Update Coupon



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "name": "Ava Chen",
  "couponLimit": "string",
  "limitDate": "string",
  "limitValue": 1,
  "type": "string",
  "discountRate": 1,
  "discountAmt": 1,
  "applyTo": "string",
  "isEnable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-coupon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "name": "Ava Chen",
    "couponLimit": "string",
    "limitDate": "string",
    "limitValue": 1,
    "type": "string",
    "discountRate": 1,
    "discountAmt": 1,
    "applyTo": "string",
    "isEnable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the coupon to update. |
| `name` | string | yes | Name of the coupon. |
| `couponLimit` | string | yes | Limit type for the coupon. |
| `limitDate` | string | yes | Date and time limit for the coupon (if couponLimit is 'date'). |
| `limitValue` | number | yes | Maximum number of times the coupon can be used (if couponLimit is 'count'). |
| `type` | string | yes | Type of discount. |
| `discountRate` | number | yes | Discount rate (percentage). |
| `discountAmt` | number | yes | Discount amount (fixed). |
| `applyTo` | string | yes | Specifies if the coupon applies to all products or specific products. |
| `isEnable` | boolean | yes | Indicates if the coupon is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Updated coupon object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/coupon/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon.md) for the provider-specific parameters and requirements.

