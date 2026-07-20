# Postpone: Schedule LinkedIn Post

Schedules a LinkedIn post in Postpone.

```
POST https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-linkedin-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-linkedin-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.text": "string",
  "variables.input.visibility": "PUBLIC",
  "variables.input.submissions[].postAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-linkedin-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.text": "string",
    "variables.input.visibility": "PUBLIC",
    "variables.input.submissions[].postAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.username` | string | yes | The username of the connected LinkedIn account to post from. |
| `variables.input.text` | string | yes | The main text content of the LinkedIn post. |
| `variables.input.visibility` | string | yes | The visibility setting for the LinkedIn post. Default: `PUBLIC`. |
| `variables.input.submissions[].postAt` | string | yes | When to publish the content in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleLinkedInPost": {
        "errors": [
          {
            "field": "https://example.com",
            "message": "https://example.com"
          }
        ],
        "post": {
          "id": "https://example.com"
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
| `scheduleLinkedInPost.errors[].field` | string |  |
| `scheduleLinkedInPost.errors[].message` | string |  |
| `scheduleLinkedInPost.post.id` | string |  |
| `scheduleLinkedInPost.success` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-linkedin-post.md) for the provider-specific parameters and requirements.

