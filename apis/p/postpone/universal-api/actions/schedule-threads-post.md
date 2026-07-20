# Postpone: Schedule Threads Post

Schedules a Threads post in Postpone.

```
POST https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-threads-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-threads-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.postAt": "string",
  "variables.input.thread[].text": "string",
  "variables.input.thread[].order": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-threads-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.postAt": "string",
    "variables.input.thread[].text": "string",
    "variables.input.thread[].order": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.username` | string | yes | The username of the connected Threads account to post from. |
| `variables.input.postAt` | string | yes | When to publish the post in ISO 8601 format. |
| `variables.input.thread[].text` | string | yes | The post text content for each item in the thread. |
| `variables.input.thread[].order` | number | yes | The 0-based position of each post in the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleThreadsPost": {
        "errors": [
          {
            "field": "string",
            "message": "string"
          }
        ],
        "post": {
          "id": "string"
        },
        "success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `scheduleThreadsPost.errors[].field` | string |  |
| `scheduleThreadsPost.errors[].message` | string |  |
| `scheduleThreadsPost.post.id` | string |  |
| `scheduleThreadsPost.success` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-threads-post.md) for the provider-specific parameters and requirements.

