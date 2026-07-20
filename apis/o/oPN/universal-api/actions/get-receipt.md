# OPN: Get Receipt

Retrieves details for a receipt from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-receipt?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-receipt?${params}`, {
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
      "company_name": "Ava Chen",
      "currency": "string",
      "customer_name": "Ava Chen",
      "id": "string",
      "issued_on": "string",
      "livemode": true,
      "location": "string",
      "number": "string",
      "object": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `currency` | string |  |
| `customer_name` | string |  |
| `id` | string |  |
| `issued_on` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `number` | string |  |
| `object` | string |  |
| `total` | number |  |

## Native endpoint

Through the native OPN API, this operation is `GET /receipts/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-receipt.md) for the provider-specific parameters and requirements.

