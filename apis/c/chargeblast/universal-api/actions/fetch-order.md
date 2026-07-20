# Chargeblast: Fetch Order

Retrieves an order from Chargeblast.

```
GET https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-order?${params}`, {
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
| `id` | string | yes | The Chargeblast order ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge": {},
      "compellingEvidence": {},
      "digitalReceipt": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge` | object | The charge details for the requested order. |
| `compellingEvidence` | object | The compelling-evidence assessment for the order. |
| `digitalReceipt` | object | The digital receipt details for the order, when available. |

## Native endpoint

Through the native Chargeblast API, this operation is `GET /api/v2/orders/:id` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-order.md) for the provider-specific parameters and requirements.

