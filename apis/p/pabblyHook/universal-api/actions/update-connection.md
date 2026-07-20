# Pabbly Hook: Update Connection



```
PUT https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/update-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/update-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "conn_ee3a07ef5a574f58abc4a2d98a5c2d3b",
  "source": {},
  "destination": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/update-connection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "conn_ee3a07ef5a574f58abc4a2d98a5c2d3b",
    "source": {},
    "destination": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionId` | string | yes | Connection ID to update. Example: `conn_ee3a07ef5a574f58abc4a2d98a5c2d3b`. |
| `name` | string | no | Connection name. Example: `Sample`. |
| `source` | object | yes | Source configuration object. |
| `destination` | object | yes | Destination configuration object. |
| `retry` | object | no | Retry configuration object. |
| `delay` | object | no | Delay configuration object. |
| `transformationId` | string | no | Transformation ID to apply. Example: `trs_672cade8d3adcf3a0d314b1b`. |
| `filter` | object | no | Connection filter configuration object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connection": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection` | object | Updated connection object. |
| `message` | string | Pabbly Hook connection update confirmation message. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `PATCH /api/v1/connections/:connectionId` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-connection.md) for the provider-specific parameters and requirements.

