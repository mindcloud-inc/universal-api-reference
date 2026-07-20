# Canny: Change Post Category

Updates a post category in Canny.

```
PUT https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postID` | string | yes |  |
| `categoryID` | string | no |  |

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

Through the native Canny API, this operation is `POST /v1/posts/change_category` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-post-category.md) for the provider-specific parameters and requirements.

