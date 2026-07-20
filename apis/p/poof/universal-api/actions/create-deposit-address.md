# Poof: Create Deposit Address

Creates a new deposit address in Poof.

```
POST https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-deposit-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-deposit-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "15",
  "crypto": "ethereum",
  "metadata.example": "dictionary"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poof/latest/actions/create-deposit-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "15",
    "crypto": "ethereum",
    "metadata.example": "dictionary"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | string | yes | Deposit address quote amount from the docs example. Default: `15`. |
| `crypto` | string | yes | Crypto asset code from the docs example. Default: `ethereum`. |
| `metadata.example` | string | yes | Nested metadata value from the docs example. Default: `dictionary`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "amount": "string",
      "charge": "string",
      "crypto": "string",
      "currency": "string",
      "rate": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `amount` | string |  |
| `charge` | string |  |
| `crypto` | string |  |
| `currency` | string |  |
| `rate` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST https://www.poof.io/api/v2/create_charge` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deposit-address.md) for the provider-specific parameters and requirements.

