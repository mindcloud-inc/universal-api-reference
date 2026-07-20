# WhautoChat: Update Broadcast by ID

Updates an existing broadcast in WhautoChat by ID.

```
PUT https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-broadcast-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-broadcast-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcastId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-broadcast-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcastId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcastId` | string | yes | Broadcast unique ID |
| `workspace.id` | string | no |  |
| `name` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string",
      "workspace": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `type` | string |  |
| `workspace.id` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `PUT /v1/broadcasts/{broadcastId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-broadcast-by-id.md) for the provider-specific parameters and requirements.

