# Tender Support: Get Discussion

Retrieves a discussion from Tender Support.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-discussion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-discussion?connectionId=$CONNECTION_ID&discussionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "discussionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-discussion?${params}`, {
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
| `discussionId` | number | yes | The Tender discussion ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorEmail": "ava@example.com",
      "authorName": "Ava Chen",
      "categoryHref": "string",
      "comments": [
        {}
      ],
      "commentsCount": 1,
      "commentsHref": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "htmlHref": "string",
      "lastAuthorEmail": "ava@example.com",
      "lastAuthorName": "Ava Chen",
      "lastCommentId": 1,
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "lastUserId": 1,
      "lastVia": "string",
      "number": 1,
      "permalink": "https://example.com",
      "public": true,
      "resolveHref": "string",
      "state": "string",
      "title": "string",
      "toggleHref": "string",
      "userHref": "string",
      "via": "string",
      "watchersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorEmail` | string |  |
| `authorName` | string |  |
| `categoryHref` | string |  |
| `comments` | array<object> |  |
| `commentsCount` | number |  |
| `commentsHref` | string |  |
| `createdAt` | date |  |
| `href` | string |  |
| `htmlHref` | string |  |
| `lastAuthorEmail` | string |  |
| `lastAuthorName` | string |  |
| `lastCommentId` | number |  |
| `lastUpdatedAt` | date |  |
| `lastUserId` | number |  |
| `lastVia` | string |  |
| `number` | number |  |
| `permalink` | string |  |
| `public` | boolean |  |
| `resolveHref` | string |  |
| `state` | string |  |
| `title` | string |  |
| `toggleHref` | string |  |
| `userHref` | string |  |
| `via` | string |  |
| `watchersCount` | number |  |

## Native endpoint

Through the native Tender Support API, this operation is `GET /discussions/:discussionId` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discussion.md) for the provider-specific parameters and requirements.

