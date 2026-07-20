# OfficeClip: List Events

Retrieves events from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-events?${params}`, {
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
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "eventName": "Ava Chen",
      "eventType": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "isAllDayEvent": true,
      "security": {
        "append": true,
        "delete": true,
        "read": true,
        "write": true
      },
      "startDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDateTime` | date |  |
| `eventName` | string |  |
| `eventType.id` | string |  |
| `eventType.name` | string |  |
| `id` | string |  |
| `isAllDayEvent` | boolean |  |
| `security.append` | boolean |  |
| `security.delete` | boolean |  |
| `security.read` | boolean |  |
| `security.write` | boolean |  |
| `startDateTime` | date |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/event-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

