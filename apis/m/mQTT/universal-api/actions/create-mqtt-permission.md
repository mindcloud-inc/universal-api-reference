# MQTT: Create MQTT Permission

Creates a new MQTT permission in HiveMQ Cloud.

```
POST https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-permission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-permission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "permission.description": "string",
  "permission.name": "Ava Chen",
  "permission.publishAllowed": true,
  "permission.qos0Allowed": true,
  "permission.qos1Allowed": true,
  "permission.qos2Allowed": true,
  "permission.retainedMsgsAllowed": true,
  "permission.subscribeAllowed": true,
  "permission.topic": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-permission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "permission.description": "string",
    "permission.name": "Ava Chen",
    "permission.publishAllowed": true,
    "permission.qos0Allowed": true,
    "permission.qos1Allowed": true,
    "permission.qos2Allowed": true,
    "permission.retainedMsgsAllowed": true,
    "permission.subscribeAllowed": true,
    "permission.topic": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `permission.description` | string | yes | Description for the new MQTT permission |
| `permission.name` | string | yes | Name for the new MQTT permission |
| `permission.publishAllowed` | boolean | yes | Whether publishing is allowed |
| `permission.qos0Allowed` | boolean | yes | Whether QoS 0 is allowed |
| `permission.qos1Allowed` | boolean | yes | Whether QoS 1 is allowed |
| `permission.qos2Allowed` | boolean | yes | Whether QoS 2 is allowed |
| `permission.retainedMsgsAllowed` | boolean | yes | Whether retained messages are allowed |
| `permission.subscribeAllowed` | boolean | yes | Whether subscribing is allowed |
| `permission.topic` | string | yes | MQTT topic filter for this permission |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissionInfo": {
        "applyTo": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "publishAllowed": true,
        "subscribeAllowed": true,
        "topic": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissionInfo.applyTo` | string |  |
| `permissionInfo.description` | string |  |
| `permissionInfo.id` | string |  |
| `permissionInfo.name` | string |  |
| `permissionInfo.publishAllowed` | boolean |  |
| `permissionInfo.subscribeAllowed` | boolean |  |
| `permissionInfo.topic` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `POST /mqtt/permissions` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mqtt-permission.md) for the provider-specific parameters and requirements.

