# Solace PubSub+: Get Service Class

Retrieves a service class from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-class
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-class?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-class?${params}`, {
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
| `id` | string | yes | Service class identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brokerScalingTier": "string",
      "highAvailabilityCapable": true,
      "id": "string",
      "limits": [
        {}
      ],
      "maxNumberVpns": 1,
      "name": "Ava Chen",
      "type": "string",
      "vpnConnections": 1,
      "vpnMaxSpoolSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brokerScalingTier` | string |  |
| `highAvailabilityCapable` | boolean |  |
| `id` | string |  |
| `limits` | array<object> |  |
| `maxNumberVpns` | number |  |
| `name` | string |  |
| `type` | string |  |
| `vpnConnections` | number |  |
| `vpnMaxSpoolSize` | number |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/serviceClasses/{id}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-class.md) for the provider-specific parameters and requirements.

