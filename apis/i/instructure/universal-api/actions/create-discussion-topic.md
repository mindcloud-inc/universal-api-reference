# Instructure: Create Discussion Topic

Creates a new discussion topic in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-discussion-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-discussion-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "1",
  "title": "MindCloud Validation Discussion"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-discussion-topic', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "1",
    "title": "MindCloud Validation Discussion"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `title` | string | yes | Discussion title. Default: `MindCloud Validation Discussion`. |
| `message` | string | no | Discussion body. |
| `published` | boolean | no | Publish immediately. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discussionType": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "lastReplyAt": "string",
      "message": "string",
      "postedAt": "string",
      "published": true,
      "requireInitialPost": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discussionType` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `lastReplyAt` | string |  |
| `message` | string |  |
| `postedAt` | string |  |
| `published` | boolean |  |
| `requireInitialPost` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `POST /courses/:course_id/discussion_topics` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-discussion-topic.md) for the provider-specific parameters and requirements.

