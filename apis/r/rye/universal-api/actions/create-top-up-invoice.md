# Rye: Create Top-Up Invoice

Creates an on-demand top-up invoice in Rye.

```
POST https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-top-up-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-top-up-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amountSubunits": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-top-up-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amountSubunits": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amountSubunits` | number | yes | Amount in smallest currency unit. |
| `chargeAutomatically` | boolean | no | Override whether to automatically charge the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "bankTransferDetails": {},
      "id": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `bankTransferDetails` | object |  |
| `id` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/billing/drawdown/topup` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-top-up-invoice.md) for the provider-specific parameters and requirements.

