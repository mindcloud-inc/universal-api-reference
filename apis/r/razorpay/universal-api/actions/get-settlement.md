# Razorpay: Get Settlement

Retrieves a settlement from Razorpay by ID.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-settlement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-settlement?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/get-settlement?${params}`, {
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
| `id` | string | yes | Unique identifier of the settlement. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": 1,
      "entity": "string",
      "fees": 1,
      "id": "string",
      "status": "string",
      "tax": 1,
      "utr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | number |  |
| `entity` | string |  |
| `fees` | number |  |
| `id` | string |  |
| `status` | string |  |
| `tax` | number |  |
| `utr` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/settlements/:id` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settlement.md) for the provider-specific parameters and requirements.

