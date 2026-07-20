# Webpushr: Send Push to Segments



```
POST https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/send-push-to-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webpushr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/send-push-to-segments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "segment[]": [
    1
  ],
  "targetUrl": "https://example.com",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/send-push-to-segments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "segment[]": [1],
    "targetUrl": "https://example.com",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoHide` | boolean | no |  |
| `expirePush` | string | no |  |
| `icon` | string | no |  |
| `image` | string | no |  |
| `message` | string | yes |  |
| `name` | string | no |  |
| `segment[]` | array<number> | yes |  |
| `sendAt` | string | no |  |
| `targetUrl` | string | yes |  |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Result message from Webpushr. |
| `id` | string | The created campaign ID when the send succeeds. |
| `status` | string | Whether the API request succeeded. |

## Native endpoint

Through the native Webpushr API, this operation is `POST /notification/send/segment` (base URL `https://api.webpushr.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-push-to-segments.md) for the provider-specific parameters and requirements.

