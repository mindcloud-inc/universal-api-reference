# CoinGate: Create Send Request

Creates a new send request in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-send-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-send-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ledgerAccountId": "string",
  "beneficiaryPayoutSettingId": 1,
  "amount": "string",
  "amountCurrencyId": 1,
  "purpose": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-send-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ledgerAccountId": "string",
    "beneficiaryPayoutSettingId": 1,
    "amount": "string",
    "amountCurrencyId": 1,
    "purpose": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ledgerAccountId` | string | yes | CoinGate ledger account ID. |
| `beneficiaryPayoutSettingId` | number | yes | CoinGate beneficiary payout setting ID. |
| `amount` | string | yes | Send request amount. |
| `amountCurrencyId` | number | yes | CoinGate amount currency ID. |
| `purpose` | string | yes | Send request purpose. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "purpose": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `purpose` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /send_requests` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-send-request.md) for the provider-specific parameters and requirements.

