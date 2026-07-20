# MQTT: Search MQTT Clients

Finds MQTT clients in HiveMQ Cloud by query parameters.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/search-mqtt-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/search-mqtt-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/search-mqtt-clients?${params}`, {
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
| `booleanFilter` | string | no | Boolean client search filter in the documented type:value format, for example CONNECTED:true. |
| `stringFilter` | string | no | String client search filter in the documented type:operation:value format, for example ID:EQ:client1. |
| `numberFilter` | string | no | Number client search filter in the documented type:operation:value format, for example MAX_QUEUE_SIZE:GT:100. |
| `limit` | number | no | Page size between 50 and 2500. HiveMQ documents 500 as the default. |
| `cursor` | string | no | Cursor returned by the previous search page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "connected": true,
          "connectedNode": "string",
          "currentQueueSize": 1,
          "id": "string",
          "ipAddress": "string",
          "maximumQueueSize": 1,
          "timestamp": 1,
          "username": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].connected` | boolean |  |
| `items[].connectedNode` | string |  |
| `items[].currentQueueSize` | number |  |
| `items[].id` | string |  |
| `items[].ipAddress` | string |  |
| `items[].maximumQueueSize` | number |  |
| `items[].timestamp` | number |  |
| `items[].username` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /a/mqtt/clients/search` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-mqtt-clients.md) for the provider-specific parameters and requirements.

