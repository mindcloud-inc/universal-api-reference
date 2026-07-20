# Particle: Update SIM



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-sim
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-sim" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "activate",
  "iccid": "89014103211118510720"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-sim', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "activate",
    "iccid": "89014103211118510720"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Default: `activate`. |
| `iccid` | string | yes | Default: `89014103211118510720`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iccid": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iccid` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Particle API, this operation is `PUT /v1/sims/:iccid` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sim.md) for the provider-specific parameters and requirements.

