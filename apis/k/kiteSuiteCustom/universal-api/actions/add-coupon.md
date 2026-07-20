# Kite Suite: Add Coupon



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "element": "string",
  "name": "Ava Chen",
  "code": "string",
  "couponLimit": 1,
  "limitDate": "string",
  "limitValue": 1,
  "type": "string",
  "discountRate": 1,
  "discountAmt": 1,
  "applyTo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/add-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "element": "string",
    "name": "Ava Chen",
    "code": "string",
    "couponLimit": 1,
    "limitDate": "string",
    "limitValue": 1,
    "type": "string",
    "discountRate": 1,
    "discountAmt": 1,
    "applyTo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `element` | string | yes | ID of the payment element to which the coupon is added. |
| `name` | string | yes | Name of the coupon. |
| `code` | string | yes | Coupon code. |
| `couponLimit` | number | yes | Maximum number of times the coupon can be used. |
| `limitDate` | string | yes | Date and time limit for the coupon. |
| `limitValue` | number | yes | Minimum value required to apply the coupon. |
| `type` | string | yes | Type of discount. |
| `discountRate` | number | yes | Discount rate (percentage). |
| `discountAmt` | number | yes | Discount amount (fixed). |
| `applyTo` | string | yes | Specifies if the coupon applies to all products or specific products. |

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
| `value` | object | Created coupon object. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/form/coupon` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-coupon.md) for the provider-specific parameters and requirements.

