# MQTT: Create MQTT Role

Creates a new MQTT role in HiveMQ Cloud.

```
POST https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "role.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "role.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `role.description` | string | no | Description for the new MQTT role |
| `role.name` | string | yes | Name for the new MQTT role |

## Response

```json
{
  "success": true,
  "data": [
    {
      "roleInfo": {
        "description": "string",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `roleInfo.description` | string |  |
| `roleInfo.id` | string |  |
| `roleInfo.name` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `POST /mqtt/roles` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mqtt-role.md) for the provider-specific parameters and requirements.

