# Swell: Update Coupon



```
PUT https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "discounts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-coupon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "discounts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Swell coupon ID. |
| `codes[]` | array<object> | no | Coupon code definitions. |
| `discounts[]` | array<object> | yes | Coupon discount rules. |
| `name` | string | no | The coupon name. |
| `active` | boolean | no | Whether the coupon is active. |
| `dateExpired` | date | no | The coupon expiration timestamp. |
| `description` | string | no | The coupon description. |
| `multiCodes` | boolean | no | Whether the coupon supports multiple codes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "codes": {
        "count": 1,
        "limit": 1,
        "page": 1,
        "pageCount": 1,
        "results": [
          {
            "code": "string",
            "dateCreated": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "parentId": "string",
            "useCount": 1,
            "useTotal": 1
          }
        ]
      },
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "discounts": [
        {
          "type": "string",
          "valuePercent": 1,
          "valueType": "string"
        }
      ],
      "id": "string",
      "multiCodes": true,
      "name": "Ava Chen",
      "useCount": 1,
      "useTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `codes.count` | number |  |
| `codes.limit` | number |  |
| `codes.page` | number |  |
| `codes.pageCount` | number |  |
| `codes.results[].code` | string |  |
| `codes.results[].dateCreated` | date |  |
| `codes.results[].id` | string |  |
| `codes.results[].parentId` | string |  |
| `codes.results[].useCount` | number |  |
| `codes.results[].useTotal` | number |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `discounts[].type` | string |  |
| `discounts[].valuePercent` | number |  |
| `discounts[].valueType` | string |  |
| `id` | string |  |
| `multiCodes` | boolean |  |
| `name` | string |  |
| `useCount` | number |  |
| `useTotal` | number |  |

## Native endpoint

Through the native Swell API, this operation is `PUT /coupons/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-coupon.md) for the provider-specific parameters and requirements.

