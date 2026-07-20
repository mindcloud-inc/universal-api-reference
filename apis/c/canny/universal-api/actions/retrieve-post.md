# Canny: Retrieve Post

Retrieves a single post from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-post?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/retrieve-post?${params}`, {
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
| `id` | string | no |  |
| `urlName` | string | no |  |
| `boardID` | string | no |  |

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
      "githubIssueIDs": [
        "string"
      ],
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
| `githubIssueIDs` | array<string> |  |
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

Through the native Canny API, this operation is `POST /v1/posts/retrieve` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-post.md) for the provider-specific parameters and requirements.

