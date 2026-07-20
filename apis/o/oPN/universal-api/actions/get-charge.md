# OPN: Get Charge

Retrieves details for a charge from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge?${params}`, {
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
| `id` | string | yes | The charge ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "authorized": true,
      "capture": true,
      "card": {},
      "created_at": "string",
      "currency": "string",
      "customer": "string",
      "description": "string",
      "failure_code": "string",
      "failure_message": "string",
      "id": "string",
      "link": "https://example.com",
      "livemode": true,
      "location": "string",
      "metadata": {},
      "object": "string",
      "paid": true,
      "paid_at": "string",
      "refunds": {},
      "source": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorized` | boolean |  |
| `capture` | boolean |  |
| `card` | object |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer` | string |  |
| `description` | string |  |
| `failure_code` | string |  |
| `failure_message` | string |  |
| `id` | string |  |
| `link` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `paid` | boolean |  |
| `paid_at` | string |  |
| `refunds` | object |  |
| `source` | object |  |
| `status` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /charges/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge.md) for the provider-specific parameters and requirements.

