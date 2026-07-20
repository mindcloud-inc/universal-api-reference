# Instructure: Delete Discussion Topic

Deletes a discussion topic from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-discussion-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-discussion-topic?connectionId=$CONNECTION_ID&courseId=1&topicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "1",
  "topicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-discussion-topic?${params}`, {
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
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `topicId` | string | yes | The Canvas discussion topic ID. Default: `1`. |

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

Through the native Instructure API, this operation is `DELETE /courses/:course_id/discussion_topics/:topic_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-discussion-topic.md) for the provider-specific parameters and requirements.

