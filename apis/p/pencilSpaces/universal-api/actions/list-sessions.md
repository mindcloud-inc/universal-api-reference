# Pencil Spaces: List Sessions



```
GET https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-sessions?${params}`, {
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
      "attendees": [
        {}
      ],
      "recordings": [
        {}
      ],
      "sessionEndTime": "string",
      "sessionId": "string",
      "sessionStartTime": "string",
      "sessionStats": {},
      "sessionTitle": "string",
      "sessionVisibility": "string",
      "spaceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> |  |
| `recordings` | array<object> |  |
| `sessionEndTime` | string |  |
| `sessionId` | string |  |
| `sessionStartTime` | string |  |
| `sessionStats` | object |  |
| `sessionTitle` | string |  |
| `sessionVisibility` | string |  |
| `spaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `GET /analytics/sessions` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

