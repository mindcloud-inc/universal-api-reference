# WhautoChat: Get Broadcast by ID

Retrieves a broadcast from WhautoChat by ID.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-by-id?connectionId=$CONNECTION_ID&broadcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcastId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-by-id?${params}`, {
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
| `broadcastId` | string | yes | Broadcast unique ID |

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

Through the native WhautoChat API, this operation is `GET /v1/broadcasts/{broadcastId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-broadcast-by-id.md) for the provider-specific parameters and requirements.

