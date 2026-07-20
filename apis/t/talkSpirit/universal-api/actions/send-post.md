# talkSpirit: Send Post

Creates a new post in talkSpirit via incoming webhook.

```
POST https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a talkSpirit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |
| `content` | string | yes |  |
| `threadId` | string | no | Optional thread identifier used to group related posts into the same discussion. |
| `url` | string | no |  |
| `contact` | object | no |  |
| `contact.displayName` | string | no |  |
| `contact.url` | string | no |  |
| `contact.icon` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Fallback output echoing the submitted message content when talkSpirit accepts the webhook without returning a body. |

## Native endpoint

Through the native talkSpirit API, this operation is `POST {{credentials.webhookUrl}}` (base URL `https://webhook.talkspirit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-post.md) for the provider-specific parameters and requirements.

