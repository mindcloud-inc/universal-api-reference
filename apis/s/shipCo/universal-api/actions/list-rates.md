# Ship&Co: List Rates



```
GET https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-rates?connectionId=$CONNECTION_ID&setup=%5Bobject%20Object%5D&to_address=%5Bobject%20Object%5D&from_address=%5Bobject%20Object%5D&products%5B%5D=%5Bobject%20Object%5D&parcels%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "setup": "[object Object]",
  "to_address": "[object Object]",
  "from_address": "[object Object]",
  "products[]": "[object Object]",
  "parcels[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-rates?${params}`, {
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
| `setup` | object | yes | Carrier and rate setup details. Do not include service for rates. |
| `to_address` | object | yes | Recipient address object. |
| `from_address` | object | yes | Sender address object. |
| `products[]` | array<object> | yes | Product line items array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parcels[]` | array<object> | yes | Parcel details array. |
| `customs` | object | no | Customs details for international rate requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrier_id": "string",
      "currency": "string",
      "errors": [
        {}
      ],
      "price": 1,
      "service": "string",
      "surcharges": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string | Carrier code. |
| `carrier_id` | string | Ship&Co carrier account ID for the returned rate. |
| `currency` | string | Rate currency. |
| `errors` | array<object> | Per-carrier rate errors returned when one or more carriers cannot quote. |
| `price` | number | Rate price. |
| `service` | string | Carrier service code. |
| `surcharges` | array<object> | Carrier surcharge details, when returned. |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /rates` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rates.md) for the provider-specific parameters and requirements.

