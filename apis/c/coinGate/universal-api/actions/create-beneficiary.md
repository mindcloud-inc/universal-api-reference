# CoinGate: Create Beneficiary

Creates a new beneficiary in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-beneficiary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-beneficiary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beneficiaryType": "string",
  "email": "ava@example.com",
  "country": "string",
  "currencyId": 1,
  "platformId": 1,
  "cryptoAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-beneficiary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beneficiaryType": "string",
    "email": "ava@example.com",
    "country": "string",
    "currencyId": 1,
    "platformId": 1,
    "cryptoAddress": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beneficiaryType` | string | yes | Beneficiary type. |
| `email` | string | yes | Beneficiary email. |
| `country` | string | yes | Beneficiary country. |
| `currencyId` | number | yes | CoinGate currency ID. |
| `platformId` | number | yes | CoinGate platform ID. |
| `cryptoAddress` | string | yes | Beneficiary crypto address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beneficiaryType": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beneficiaryType` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `surname` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /beneficiaries` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-beneficiary.md) for the provider-specific parameters and requirements.

