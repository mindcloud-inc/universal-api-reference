# Postpone: Schedule Reddit Post

Schedules a Reddit post in Postpone.

```
POST https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-reddit-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-reddit-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.title": "string",
  "variables.input.content": "string",
  "variables.input.submissions[].validationId": "sub1",
  "variables.input.submissions[].subreddit": "string",
  "variables.input.submissions[].postAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-reddit-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.title": "string",
    "variables.input.content": "string",
    "variables.input.submissions[].validationId": "sub1",
    "variables.input.submissions[].subreddit": "string",
    "variables.input.submissions[].postAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.username` | string | yes | The username of the connected Reddit account to post from. |
| `variables.input.title` | string | yes | The title of the Reddit post. |
| `variables.input.content` | string | yes | The text content for the Reddit post. |
| `variables.input.submissions[].validationId` | string | yes | Internal submission identifier used for validation mapping. Default: `sub1`. |
| `variables.input.submissions[].subreddit` | string | yes | The subreddit name without the r/ prefix. |
| `variables.input.submissions[].postAt` | string | yes | When to publish the content in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleRedditPost": {
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
| `scheduleRedditPost.errors[].field` | string |  |
| `scheduleRedditPost.errors[].message` | string |  |
| `scheduleRedditPost.post.id` | string |  |
| `scheduleRedditPost.success` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-reddit-post.md) for the provider-specific parameters and requirements.

