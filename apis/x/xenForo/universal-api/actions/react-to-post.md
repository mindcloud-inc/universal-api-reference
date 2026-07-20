# XenForo: React To Post

Creates a reaction on a post in XenForo.

```
POST https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/react-to-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/react-to-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "456",
  "reactionId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/react-to-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "456",
    "reactionId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the post to react to. Example: `456`. |
| `reactionId` | number | yes | ID of the reaction to use. Use the current reaction ID to undo. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | insert or delete, depending on whether the reaction was added or removed. |
| `success` | boolean |  |

## Native endpoint

Through the native XenForo API, this operation is `POST /posts/:id/react` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/react-to-post.md) for the provider-specific parameters and requirements.

