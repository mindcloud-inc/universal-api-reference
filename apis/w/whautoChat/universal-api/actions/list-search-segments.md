# WhautoChat: List/Search Segments

Finds segments in WhautoChat.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-search-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-search-segments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-search-segments?${params}`, {
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
| `workspaceId` | string | no | Filter by workspace ID |
| `searchText` | string | no | Free text search |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "retargetBroadcast": {
        "id": "string"
      },
      "retargetEngagementType": "string",
      "scheduleDateTime": "2026-05-07T12:00:00.000Z",
      "segments": [
        {}
      ],
      "startedAt": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `retargetBroadcast.id` | string |  |
| `retargetEngagementType` | string |  |
| `scheduleDateTime` | date |  |
| `segments` | array<object> |  |
| `startedAt` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/segments` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-search-segments.md) for the provider-specific parameters and requirements.

