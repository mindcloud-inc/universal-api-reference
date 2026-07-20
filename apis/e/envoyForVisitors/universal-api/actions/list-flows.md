# Envoy for Visitors: List Flows

Finds flows in Envoy for Visitors.

```
GET https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-flows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/list-flows?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "locationId": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `locationId` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `GET /flows` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flows.md) for the provider-specific parameters and requirements.

