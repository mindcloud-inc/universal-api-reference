# Canny: Change Post Status

Updates a post status in Canny.

```
PUT https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "changerID": "string",
  "postID": "string",
  "status": "string",
  "shouldNotifyVoters": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "changerID": "string",
    "postID": "string",
    "status": "string",
    "shouldNotifyVoters": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `changerID` | string | yes |  |
| `postID` | string | yes |  |
| `status` | string | yes |  |
| `shouldNotifyVoters` | boolean | yes |  |
| `commentValue` | string | no |  |
| `commentImageURLs` | list<string> | no |  |

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
      "changeComment": {},
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
| `changeComment` | object |  |
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

Through the native Canny API, this operation is `POST /v1/posts/change_status` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-post-status.md) for the provider-specific parameters and requirements.

