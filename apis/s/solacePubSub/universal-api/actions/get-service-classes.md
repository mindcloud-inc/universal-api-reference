# Solace PubSub+: Get Service Classes

Retrieves service classes from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-classes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-service-classes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/serviceClasses` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-service-classes.md) for the provider-specific parameters and requirements.

