# CoinGate: Get Conversion

Retrieves a currency conversion from CoinGate by ID.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-conversion?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-conversion?${params}`, {
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
| `id` | string | yes | CoinGate conversion ID. |

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

Through the native CoinGate API, this operation is `GET /ledger/conversions/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversion.md) for the provider-specific parameters and requirements.

