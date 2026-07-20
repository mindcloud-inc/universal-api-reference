# Soundee: List Cart Abandonments

Retrieves abandoned cart records from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-cart-abandonments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-cart-abandonments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-cart-abandonments?${params}`, {
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
| `listType` | string | no | Filter abandoned carts by state. |
| `search` | string | no | Search by customer name, email, token, or price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "contact": {},
      "country": {},
      "coupon": {},
      "created": 1,
      "currency": {},
      "discount": 1,
      "grandTotal": 1,
      "id": 1,
      "itemCount": 1,
      "items": [
        {}
      ],
      "lastActivity": "string",
      "lastCartActivity": "string",
      "parameters": {},
      "recoverable": 1,
      "status": "string",
      "store": {},
      "subTotal": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `contact` | object |  |
| `country` | object |  |
| `coupon` | object |  |
| `created` | number |  |
| `currency` | object |  |
| `discount` | number |  |
| `grandTotal` | number |  |
| `id` | number |  |
| `itemCount` | number |  |
| `items` | array<object> |  |
| `lastActivity` | string |  |
| `lastCartActivity` | string |  |
| `parameters` | object |  |
| `recoverable` | number |  |
| `status` | string |  |
| `store` | object |  |
| `subTotal` | number |  |
| `token` | string |  |

## Native endpoint

Through the native Soundee API, this operation is `GET /cart-abandonments` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cart-abandonments.md) for the provider-specific parameters and requirements.

