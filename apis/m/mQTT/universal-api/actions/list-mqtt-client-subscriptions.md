# MQTT: List MQTT Client Subscriptions

Retrieves subscriptions for an MQTT client in HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-client-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-client-subscriptions?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-client-subscriptions?${params}`, {
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
      "_links": {
        "next": "https://example.com"
      },
      "items": [
        {
          "noLocal": true,
          "qos": "string",
          "retainAsPublished": true,
          "retainHandling": "string",
          "subscriptionIdentifier": 1,
          "topicFilter": "string"
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
| `_links.next` | string |  |
| `items[].noLocal` | boolean |  |
| `items[].qos` | string |  |
| `items[].retainAsPublished` | boolean |  |
| `items[].retainHandling` | string |  |
| `items[].subscriptionIdentifier` | number |  |
| `items[].topicFilter` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/clients/:clientId/subscriptions` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mqtt-client-subscriptions.md) for the provider-specific parameters and requirements.

