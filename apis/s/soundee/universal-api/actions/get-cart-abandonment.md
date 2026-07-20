# Soundee: Get Cart Abandonment

Retrieves an abandoned cart from Soundee by ID or token.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-cart-abandonment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-cart-abandonment?connectionId=$CONNECTION_ID&idOrToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-cart-abandonment?${params}`, {
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
| `idOrToken` | string | yes | The ID or token of the abandoned cart. |

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

Through the native Soundee API, this operation is `GET /cart-abandonments/:idOrToken` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cart-abandonment.md) for the provider-specific parameters and requirements.

