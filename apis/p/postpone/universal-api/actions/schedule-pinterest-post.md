# Postpone: Schedule Pinterest Post

Schedules a Pinterest post in Postpone.

```
POST https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-pinterest-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-pinterest-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.title": "string",
  "variables.input.mediaUrl": "https://example.com",
  "variables.input.boardId": "string",
  "variables.input.submissions[].postAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-pinterest-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.title": "string",
    "variables.input.mediaUrl": "https://example.com",
    "variables.input.boardId": "string",
    "variables.input.submissions[].postAt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.username` | string | yes | The username of the connected Pinterest account to post from. |
| `variables.input.title` | string | yes | The title of the Pinterest pin. |
| `variables.input.description` | string | no | The description for the Pinterest pin. |
| `variables.input.link` | string | no | The URL the Pinterest pin should link to. |
| `variables.input.mediaUrl` | string | yes | URL of an image to upload and use for the pin. |
| `variables.input.boardId` | string | yes | The Pinterest board ID to pin to. |
| `variables.input.submissions[].postAt` | string | yes | When to publish the pin in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schedulePinterestPost": {
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
| `schedulePinterestPost.errors[].field` | string |  |
| `schedulePinterestPost.errors[].message` | string |  |
| `schedulePinterestPost.post.id` | string |  |
| `schedulePinterestPost.success` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-pinterest-post.md) for the provider-specific parameters and requirements.

