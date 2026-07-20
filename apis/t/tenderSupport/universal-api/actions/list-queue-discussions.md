# Tender Support: List Queue Discussions

Retrieves discussions from a Tender Support queue.

```
GET https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-queue-discussions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-queue-discussions?connectionId=$CONNECTION_ID&queueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/list-queue-discussions?${params}`, {
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
| `queueId` | string | yes | The queue ID or the special value 'mine'. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorEmail": "ava@example.com",
      "authorName": "Ava Chen",
      "categoryHref": "string",
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

Through the native Tender Support API, this operation is `GET /queues/:queueId/discussions` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queue-discussions.md) for the provider-specific parameters and requirements.

