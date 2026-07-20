# CoinGate: Create Billing Contact

Creates a new billing contact in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactType": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-billing-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactType": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactType` | string | yes | Billing contact type. |
| `email` | string | yes | Billing contact email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactType": "string",
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
| `contactType` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `surname` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /billing/contacts` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-billing-contact.md) for the provider-specific parameters and requirements.

