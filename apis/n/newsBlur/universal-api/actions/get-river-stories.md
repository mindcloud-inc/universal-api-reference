# NewsBlur: Get River Stories

Retrieves stories from multiple feeds in NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-river-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-river-stories?connectionId=$CONNECTION_ID&feedId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-river-stories?${params}`, {
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
| `feedId` | number | yes | Feed ID to include in the River of News. NewsBlur supports repeating feeds for multiple feeds. |
| `order` | string | no | Story order: newest or oldest. One of: `0`, `1`. |
| `readFilter` | string | no | Show all stories or only unread stories. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFilterStart` | date | no | Only include stories published on or after this date in YYYY-MM-DD format. |
| `dateFilterEnd` | date | no | Only include stories published on or before this date in YYYY-MM-DD format. |
| `includeHidden` | boolean | no | Include hidden stories. |
| `query` | string | no | Search keyword or phrase in the folder. NewsBlur notes feed search is premium-only. |
| `infrequent` | string | no | Show only stories from infrequently published sites, using a stories-per-month value or false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "classifiers": {},
      "code": 1,
      "elapsed_time": 1,
      "hidden_stories_removed": 1,
      "message": "string",
      "result": "string",
      "stories": [
        {}
      ],
      "user_id": 1,
      "user_profiles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `classifiers` | object | Feed intelligence classifiers. |
| `code` | number | NewsBlur result code. |
| `elapsed_time` | number | Server processing time. |
| `hidden_stories_removed` | number | Count of hidden stories removed. |
| `message` | string | Status message. |
| `result` | string | Result status. |
| `stories` | array<object> | River stories. |
| `user_id` | number | Authenticated NewsBlur user ID. |
| `user_profiles` | array<object> | Related user profiles. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/river_stories` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-river-stories.md) for the provider-specific parameters and requirements.

