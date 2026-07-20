# CoinGate: Create Conversion

Creates a new currency conversion in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ledgerAccountId": "string",
  "quoteCurrencyId": 1,
  "baseAmount": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ledgerAccountId": "string",
    "quoteCurrencyId": 1,
    "baseAmount": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ledgerAccountId` | string | yes | CoinGate ledger account ID. |
| `quoteCurrencyId` | number | yes | CoinGate quote currency ID. |
| `baseAmount` | string | yes | Conversion base amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseAmount": "string",
      "baseLedgerAccount": {
        "balance": "string",
        "id": "string"
      },
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
| `baseAmount` | string |  |
| `baseLedgerAccount.balance` | string |  |
| `baseLedgerAccount.id` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /ledger/conversions` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-conversion.md) for the provider-specific parameters and requirements.

