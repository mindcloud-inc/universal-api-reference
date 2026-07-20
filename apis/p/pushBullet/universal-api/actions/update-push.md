# Pushbullet: Update Push

Updates an existing push in Pushbullet.

```
PUT https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "push_iden": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/update-push', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "push_iden": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `push_iden` | string | yes | Push identifier to update. |
| `dismissed` | boolean | no | Set true to dismiss a push, false to undismiss. |
| `items[]` | array<object> | no | Array of update entries for mirrored notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "body": "string",
      "created": 1,
      "dismissed": true,
      "fileName": "Ava Chen",
      "fileType": "string",
      "fileUrl": "https://example.com",
      "iden": "string",
      "modified": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `body` | string |  |
| `created` | number |  |
| `dismissed` | boolean |  |
| `fileName` | string |  |
| `fileType` | string |  |
| `fileUrl` | string |  |
| `iden` | string |  |
| `modified` | number |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `POST /pushes/:push_iden` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-push.md) for the provider-specific parameters and requirements.

