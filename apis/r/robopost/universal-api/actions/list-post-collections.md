# Robopost: List Post Collections

Retrieves post collections from Robopost.

```
GET https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-post-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-post-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-post-collections?${params}`, {
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
      "automationId": "string",
      "color": "string",
      "deletePostAfterPosting": true,
      "id": "string",
      "isRecur": true,
      "name": "Ava Chen",
      "nextScheduledPost": {},
      "nextScheduledPostId": "string",
      "postingStrategy": "string",
      "postsCount": 1,
      "recurDt": "2026-05-07T12:00:00.000Z",
      "recurInterval": "string",
      "recurIntervalTimeSlots": [
        "string"
      ],
      "recurIntervalWeeklyTimeSlots": [
        "string"
      ],
      "recurUntilDt": "2026-05-07T12:00:00.000Z",
      "recurUntilDtEnabled": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automationId` | string | Automation ID. |
| `color` | string | Collection color. |
| `deletePostAfterPosting` | boolean | Whether posts are deleted after publishing. |
| `id` | string | Post collection ID. |
| `isRecur` | boolean | Whether the collection recurs. |
| `name` | string | Collection name. |
| `nextScheduledPost` | object | Next scheduled post object. |
| `nextScheduledPostId` | string | Next scheduled post ID. |
| `postingStrategy` | string | Posting strategy. |
| `postsCount` | number | Number of posts in the collection. |
| `recurDt` | date | Next recurrence datetime. |
| `recurInterval` | string | Recurrence interval. |
| `recurIntervalTimeSlots` | array<string> | Recurring time slots. |
| `recurIntervalWeeklyTimeSlots` | array<string> | Weekly recurring time slots. |
| `recurUntilDt` | date | Recurrence end datetime. |
| `recurUntilDtEnabled` | boolean | Whether recurrence end is enabled. |
| `timezone` | string | Collection timezone. |

## Native endpoint

Through the native Robopost API, this operation is `GET /post_collections/` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-collections.md) for the provider-specific parameters and requirements.

