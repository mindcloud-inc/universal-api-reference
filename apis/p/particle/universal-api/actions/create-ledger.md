# Particle: Create Ledger



```
POST https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-ledger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-ledger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ledger": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-ledger', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ledger": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ledger` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ledger": {
        "description": "string",
        "direction": "string",
        "name": "Ava Chen",
        "scope": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ledger.description` | string |  |
| `ledger.direction` | string |  |
| `ledger.name` | string |  |
| `ledger.scope` | string |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/ledgers` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ledger.md) for the provider-specific parameters and requirements.

