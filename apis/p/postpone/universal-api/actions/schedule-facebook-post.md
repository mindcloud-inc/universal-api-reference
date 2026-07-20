# Postpone: Schedule Facebook Post

Schedules a Facebook post in Postpone.

```
POST https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-facebook-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-facebook-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input.username": "Ava Chen",
  "variables.input.submissions[].postAt": "string",
  "variables.input.submissions[].mediaType": "POST"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postpone/latest/actions/schedule-facebook-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input.username": "Ava Chen",
    "variables.input.submissions[].postAt": "string",
    "variables.input.submissions[].mediaType": "POST"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.username` | string | yes | The username of the connected Facebook account to post from. |
| `variables.input.text` | string | no | The main text content of the Facebook post. |
| `variables.input.submissions[].postAt` | string | yes | When to publish the content in ISO 8601 format. |
| `variables.input.submissions[].mediaType` | string | yes | Type of Facebook content to schedule. Default: `POST`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "scheduleFacebookPost": {
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
| `scheduleFacebookPost.errors[].field` | string |  |
| `scheduleFacebookPost.errors[].message` | string |  |
| `scheduleFacebookPost.post.id` | string |  |
| `scheduleFacebookPost.success` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-facebook-post.md) for the provider-specific parameters and requirements.

