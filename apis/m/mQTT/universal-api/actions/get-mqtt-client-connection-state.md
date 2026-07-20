# MQTT: Get MQTT Client Connection State

Retrieves an MQTT client's connection state from HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client-connection-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client-connection-state?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-client-connection-state?${params}`, {
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
      "connection": {
        "connected": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection.connected` | boolean |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/clients/:clientId/connection` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mqtt-client-connection-state.md) for the provider-specific parameters and requirements.

