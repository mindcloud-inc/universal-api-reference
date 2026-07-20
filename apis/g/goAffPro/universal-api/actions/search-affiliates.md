# GoAffPro: Search Affiliates

Finds affiliates in GoAffPro by keyword.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/search-affiliates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/search-affiliates?connectionId=$CONNECTION_ID&searchIn%5B%5D=string&keyword=string&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchIn[]": "string",
  "keyword": "string",
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/search-affiliates?${params}`, {
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
| `searchIn[]` | array<string> | yes | Affiliate fields to search in. |
| `keyword` | string | yes | Search keyword. |
| `fields[]` | array<string> | yes | Fields to include in the returned affiliate records. |

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

Through the native GoAffPro API, this operation is `GET /admin/affiliates/search` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-affiliates.md) for the provider-specific parameters and requirements.

