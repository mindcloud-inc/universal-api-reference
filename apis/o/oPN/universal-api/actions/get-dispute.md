# OPN: Get Dispute

Retrieves details for a dispute from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute?${params}`, {
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
| `id` | string | yes | The dispute ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_message": "string",
      "amount": 1,
      "charge": "string",
      "closed_at": "string",
      "created_at": "string",
      "currency": "string",
      "documents": {},
      "funding_amount": 1,
      "funding_currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "message": "string",
      "metadata": {},
      "object": "string",
      "reason_code": "string",
      "reason_message": "string",
      "status": "string",
      "transactions": [
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
| `admin_message` | string |  |
| `amount` | number |  |
| `charge` | string |  |
| `closed_at` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `documents` | object |  |
| `funding_amount` | number |  |
| `funding_currency` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `reason_code` | string |  |
| `reason_message` | string |  |
| `status` | string |  |
| `transactions` | array<object> |  |

## Native endpoint

Through the native OPN API, this operation is `GET /disputes/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dispute.md) for the provider-specific parameters and requirements.

