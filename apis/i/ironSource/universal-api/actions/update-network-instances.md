# ironSource: Update Network Instances

Updates existing network instances in ironSource.

```
PUT https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/update-network-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/update-network-instances" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/update-network-instances', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appKey` | string | no | Application key as seen on the LevelPlay platform. |
| `instances` | string | no | Array of network instance objects to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | HTTP 200 success status; the official docs do not define a response body. |

## Native endpoint

Through the native ironSource API, this operation is `PUT levelPlay/network/instances/v4/:appKey` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-network-instances.md) for the provider-specific parameters and requirements.

