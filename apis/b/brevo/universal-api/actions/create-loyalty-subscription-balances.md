# Brevo: Create Loyalty Subscription Balances



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-loyalty-subscription-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-loyalty-subscription-balances" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "string",
  "pid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-loyalty-subscription-balances', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "string",
    "pid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cid` | string | yes |  |
| `pid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/loyalty/balance/programs/:pid/subscriptions/:cid/balances` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-loyalty-subscription-balances.md) for the provider-specific parameters and requirements.

