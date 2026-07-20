# CoinGate: Create Billing Request

Creates a new billing request in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billingContactId": 1,
  "currencyId": 1,
  "receiveCurrencyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billingContactId": 1,
    "currencyId": 1,
    "receiveCurrencyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingContactId` | number | yes | CoinGate billing contact ID. |
| `currencyId` | number | yes | CoinGate currency ID. |
| `receiveCurrencyId` | number | yes | CoinGate receive currency ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dueDays": 1,
      "id": 1,
      "status": "string",
      "title": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dueDays` | number |  |
| `id` | number |  |
| `status` | string |  |
| `title` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /billing/requests` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-billing-request.md) for the provider-specific parameters and requirements.

