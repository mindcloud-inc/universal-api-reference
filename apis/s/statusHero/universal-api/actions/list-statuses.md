# Status Hero: List statuses



```
GET https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/list-statuses?${params}`, {
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
      "answers": {},
      "attachments": [
        {}
      ],
      "blocked": true,
      "commentIds": [
        "string"
      ],
      "completedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "previousCompleted": true,
      "reactionIds": [
        "string"
      ],
      "reportDate": "2026-05-07T12:00:00.000Z",
      "reportId": "string",
      "slug": "string",
      "statusActivityIds": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | object |  |
| `attachments` | array<object> |  |
| `blocked` | boolean |  |
| `commentIds` | array<string> |  |
| `completedAt` | date |  |
| `id` | string |  |
| `previousCompleted` | boolean |  |
| `reactionIds` | array<string> |  |
| `reportDate` | date |  |
| `reportId` | string |  |
| `slug` | string |  |
| `statusActivityIds` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Status Hero API, this operation is `GET /statuses` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statuses.md) for the provider-specific parameters and requirements.

