# Action1: List Audit Events

Retrieves audit trail events from Action1.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-audit-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-audit-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-audit-events?${params}`, {
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
      "description": "string",
      "event": "string",
      "id": "string",
      "objectName": "Ava Chen",
      "objectUrl": "https://example.com",
      "orgId": "string",
      "orgName": "Ava Chen",
      "self": "string",
      "statusMessage": "string",
      "timestamp": "string",
      "type": "string",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `event` | string |  |
| `id` | string |  |
| `objectName` | string |  |
| `objectUrl` | string |  |
| `orgId` | string |  |
| `orgName` | string |  |
| `self` | string |  |
| `statusMessage` | string |  |
| `timestamp` | string |  |
| `type` | string |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /audit/events` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audit-events.md) for the provider-specific parameters and requirements.

