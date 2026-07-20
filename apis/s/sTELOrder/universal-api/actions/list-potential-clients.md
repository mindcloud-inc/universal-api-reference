# STEL Order: List Potential Clients

Retrieves a list of potential clients from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-potential-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-potential-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-potential-clients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bank-account": {},
      "creation-date": "string",
      "currency-code": "string",
      "deleted": true,
      "discount-percentage": 1,
      "email": "ava@example.com",
      "full-reference": "string",
      "id": 1,
      "income-tax-enabled": true,
      "legal-name": "Ava Chen",
      "main-address": {},
      "name": "Ava Chen",
      "path": "string",
      "payment-adjustment": "string",
      "phone": "string",
      "primary-tax-enabled": true,
      "reference": "string",
      "secondary-tax-enabled": true,
      "serial-number-id": 1,
      "serial-number-path": "string",
      "special-prices": [
        "string"
      ],
      "tax-identification-number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bank-account` | object |  |
| `creation-date` | string |  |
| `currency-code` | string |  |
| `deleted` | boolean |  |
| `discount-percentage` | number |  |
| `email` | string |  |
| `full-reference` | string |  |
| `id` | number |  |
| `income-tax-enabled` | boolean |  |
| `legal-name` | string |  |
| `main-address` | object |  |
| `name` | string |  |
| `path` | string |  |
| `payment-adjustment` | string |  |
| `phone` | string |  |
| `primary-tax-enabled` | boolean |  |
| `reference` | string |  |
| `secondary-tax-enabled` | boolean |  |
| `serial-number-id` | number |  |
| `serial-number-path` | string |  |
| `special-prices` | array |  |
| `tax-identification-number` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /potentialClients` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-potential-clients.md) for the provider-specific parameters and requirements.

