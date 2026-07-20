# Canny: List Posts

Retrieves all available posts from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-posts?${params}`, {
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
| `boardID` | string | no |  |
| `authorID` | string | no |  |
| `companyID` | string | no |  |
| `tagIDs` | list<string> | no |  |
| `search` | string | no |  |
| `status` | string | no |  |
| `sort` | string | no |  |
| `limit` | number | no |  |
| `skip` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "board": {},
      "by": {},
      "category": {},
      "clickup": {},
      "commentCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "details": "string",
      "eta": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "idea": {},
      "imageURLs": [
        "https://example.com"
      ],
      "jira": {},
      "linear": {},
      "mergeHistory": [
        {}
      ],
      "owner": {},
      "roadmaps": [
        {}
      ],
      "score": 1,
      "status": "string",
      "statusChangedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        {}
      ],
      "title": "string",
      "totalMRR": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `board` | object |  |
| `by` | object |  |
| `category` | object |  |
| `clickup` | object |  |
| `commentCount` | number |  |
| `created` | date |  |
| `customFields` | array<object> |  |
| `details` | string |  |
| `eta` | date |  |
| `id` | string |  |
| `idea` | object |  |
| `imageURLs` | array<string> |  |
| `jira` | object |  |
| `linear` | object |  |
| `mergeHistory` | array<object> |  |
| `owner` | object |  |
| `roadmaps` | array<object> |  |
| `score` | number |  |
| `status` | string |  |
| `statusChangedAt` | date |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `totalMRR` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/posts/list` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

