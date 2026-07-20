# Particle: Update Ledger Instance



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instance": {},
  "ledgerName": "Ava Chen",
  "scopeValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-ledger-instance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instance": {},
    "ledgerName": "Ava Chen",
    "scopeValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instance` | object | yes |  |
| `ledgerName` | string | yes |  |
| `scopeValue` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "instance": {
        "data": {},
        "name": "Ava Chen",
        "scope": {
          "type": "string"
        },
        "size_bytes": 1,
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `instance.data` | object |  |
| `instance.name` | string |  |
| `instance.scope.type` | string |  |
| `instance.size_bytes` | number |  |
| `instance.version` | string |  |

## Native endpoint

Through the native Particle API, this operation is `PUT /v1/ledgers/:ledgerName/instances/:scopeValue` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ledger-instance.md) for the provider-specific parameters and requirements.

