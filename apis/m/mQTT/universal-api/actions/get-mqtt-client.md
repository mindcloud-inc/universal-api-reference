# MQTT: Get MQTT Client

Retrieves MQTT client details from HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | MQTT client identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "connected": true,
        "connectedAt": "2026-05-07T12:00:00.000Z",
        "connection": {
          "cleanStart": true,
          "connectedListenerId": "string",
          "connectedNodeId": "string",
          "keepAlive": 1,
          "mqttVersion": "string",
          "sourceIp": "string",
          "username": "Ava Chen"
        },
        "id": "string",
        "messageQueueSize": 1,
        "restrictions": {
          "maxMessageSize": 1,
          "maxQueueSize": 1,
          "queuedMessageStrategy": "string"
        },
        "sessionExpiryInterval": 1,
        "willPresent": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.connected` | boolean |  |
| `client.connectedAt` | date |  |
| `client.connection.cleanStart` | boolean |  |
| `client.connection.connectedListenerId` | string |  |
| `client.connection.connectedNodeId` | string |  |
| `client.connection.keepAlive` | number |  |
| `client.connection.mqttVersion` | string |  |
| `client.connection.sourceIp` | string |  |
| `client.connection.username` | string |  |
| `client.id` | string |  |
| `client.messageQueueSize` | number |  |
| `client.restrictions.maxMessageSize` | number |  |
| `client.restrictions.maxQueueSize` | number |  |
| `client.restrictions.queuedMessageStrategy` | string |  |
| `client.sessionExpiryInterval` | number |  |
| `client.willPresent` | boolean |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/clients/:clientId` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mqtt-client.md) for the provider-specific parameters and requirements.

