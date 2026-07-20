# Particle: Update Logic Function



```
PUT https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-logic-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Particle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-logic-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logic_function": {
    "name": "MC Particle Logic Default Updated",
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
  },
  "logicFunctionId": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/update-logic-function', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logic_function": {"name":"MC Particle Logic Default Updated","source":{"code":"export default function main() {}","type":"JavaScript"},"enabled":false,"description":"","logic_triggers":[{"cron":"0 0 0 0 0","type":"Scheduled","enabled":true}]},
    "logicFunctionId": "00000000-0000-0000-0000-000000000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logic_function` | object | yes | Provide a full logic_function object including `name`, `description`, `enabled`, `source`, and `logic_triggers`. Default: `{"name":"MC Particle Logic Default Updated","source":{"code":"export default function main() {}","type":"JavaScript"},"enabled":false,"description":"","logic_triggers":[{"cron":"0 0 0 0 0","type":"Scheduled","enabled":true}]}`. |
| `logicFunctionId` | string | yes | Default: `00000000-0000-0000-0000-000000000000`. |

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

Through the native Particle API, this operation is `PUT /v1/logic/functions/:logicFunctionId` (base URL `https://api.particle.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-logic-function.md) for the provider-specific parameters and requirements.

