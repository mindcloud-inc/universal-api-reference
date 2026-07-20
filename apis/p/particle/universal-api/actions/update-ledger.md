# Particle: Update Ledger



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ledger": {},
  "ledgerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ledger": {},
    "ledgerName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ledger` | object | yes |  |
| `ledgerName` | string | yes |  |

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
        "scope": "string",
        "stats": {
          "instance_count": 1,
          "total_bytes": 1
        }
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
| `ledger.stats.instance_count` | number |  |
| `ledger.stats.total_bytes` | number |  |

## Native endpoint

Through the native Particle API, this operation is `PUT /v1/ledgers/:ledgerName` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ledger.md) for the provider-specific parameters and requirements.

