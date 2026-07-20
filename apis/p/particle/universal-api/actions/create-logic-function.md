# Particle: Create Logic Function



```
POST https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-logic-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-logic-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logic_function": {
    "name": "MC Particle Logic Default",
    "source": {
      "code": "export default function main() {}",
      "type": "JavaScript"
    },
    "enabled": false,
    "description": "",
    "logic_triggers": [
      {
        "cron": "0 0 0 0 0",
        "type": "Scheduled",
        "enabled": true
      }
    ]
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/create-logic-function', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logic_function": {"name":"MC Particle Logic Default","source":{"code":"export default function main() {}","type":"JavaScript"},"enabled":false,"description":"","logic_triggers":[{"cron":"0 0 0 0 0","type":"Scheduled","enabled":true}]}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logic_function` | object | yes | Provide a full logic_function object including `name`, `description`, `enabled`, `source`, and `logic_triggers`. Default: `{"name":"MC Particle Logic Default","source":{"code":"export default function main() {}","type":"JavaScript"},"enabled":false,"description":"","logic_triggers":[{"cron":"0 0 0 0 0","type":"Scheduled","enabled":true}]}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Particle API, this operation is `POST /v1/logic/functions` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-logic-function.md) for the provider-specific parameters and requirements.

