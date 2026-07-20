# TrueLayer: Create Payout

Creates a payout in TrueLayer.

```
POST https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/create-payout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_in_minor": 1,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_in_minor` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `POST /v3/payouts` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout.md) for the provider-specific parameters and requirements.

