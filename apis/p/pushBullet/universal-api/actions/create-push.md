# Pushbullet: Create Push

Creates a new push in Pushbullet.

```
POST https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/create-push', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Push type (note, link, file). |
| `title` | string | no | Push title. |
| `body` | string | no | Push body content. |
| `url` | string | no | URL for link pushes. |
| `file_name` | string | no | Name of the uploaded file for file pushes. |
| `file_type` | string | no | MIME type of the uploaded file for file pushes. |
| `file_url` | string | no | Uploaded file URL returned from upload-request. |

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

Through the native Pushbullet API, this operation is `POST /pushes` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-push.md) for the provider-specific parameters and requirements.

