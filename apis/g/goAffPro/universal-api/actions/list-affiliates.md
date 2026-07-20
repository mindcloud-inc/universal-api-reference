# GoAffPro: List Affiliates

Retrieves a list of affiliates from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates?connectionId=$CONNECTION_ID&limit=25&offset=0&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates?${params}`, {
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
| `email` | string | no | Only return affiliates matching this email address. |
| `fields[]` | array<string> | yes | Fields to include in the returned affiliate records. |
| `status` | string | no | Only return affiliates with this status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commission": {
        "amount": 1,
        "on": "string",
        "type": "string"
      },
      "country": "string",
      "coupon": "string",
      "coupons": [
        {
          "code": "string",
          "discountType": "string",
          "discountValue": 1
        }
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "groupId": 1,
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "paymentMethod": "string",
      "phone": "string",
      "refCode": "string",
      "refCodes": [
        {
          "response": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commission.amount` | number |  |
| `commission.on` | string |  |
| `commission.type` | string |  |
| `country` | string |  |
| `coupon` | string |  |
| `coupons[].code` | string |  |
| `coupons[].discountType` | string |  |
| `coupons[].discountValue` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `groupId` | number |  |
| `id` | number | Affiliate id of the affiliate |
| `lastName` | string |  |
| `name` | string |  |
| `paymentMethod` | string |  |
| `phone` | string |  |
| `refCode` | string |  |
| `refCodes[].response` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/affiliates` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-affiliates.md) for the provider-specific parameters and requirements.

