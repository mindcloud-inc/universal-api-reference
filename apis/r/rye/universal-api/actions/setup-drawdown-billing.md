# Rye: Setup Drawdown Billing

Updates drawdown billing settings in Rye.

```
PUT https://connect.mindcloud.co/v1/universal/rye/latest/actions/setup-drawdown-billing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rye/latest/actions/setup-drawdown-billing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "minBalanceSubunits": 1,
  "targetBalanceSubunits": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/setup-drawdown-billing', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "minBalanceSubunits": 1,
    "targetBalanceSubunits": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chargeAutomatically` | boolean | no | Whether to automatically charge the invoice when created. |
| `minBalanceSubunits` | number | yes | Minimum balance threshold in smallest currency unit. |
| `targetBalanceSubunits` | number | yes | Target balance in smallest currency unit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "drawdown": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `drawdown` | object |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/billing/drawdown` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/setup-drawdown-billing.md) for the provider-specific parameters and requirements.

