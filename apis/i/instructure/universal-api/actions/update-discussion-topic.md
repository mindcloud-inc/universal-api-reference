# Instructure: Update Discussion Topic

Updates an existing discussion topic in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-discussion-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-discussion-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "1",
  "topicId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-discussion-topic', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "1",
    "topicId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `topicId` | string | yes | The Canvas discussion topic ID. Default: `1`. |
| `title` | string | no | Discussion title. |
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

Through the native Instructure API, this operation is `PUT /courses/:course_id/discussion_topics/:topic_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-discussion-topic.md) for the provider-specific parameters and requirements.

