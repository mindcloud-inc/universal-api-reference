# Sendible: Create Upload Intent



```
POST https://connect.mindcloud.co/v1/universal/sendible/latest/actions/create-upload-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/create-upload-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source.type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendible/latest/actions/create-upload-intent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source.type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source.contentType` | string | no | Original MIME type for file uploads. |
| `source.filename` | string | no | Original filename for file uploads. |
| `source.size` | number | no | Original file size in bytes. |
| `source.type` | string | yes | Upload source type, for example File or Url. |
| `source.url` | string | no | Remote URL when creating an upload intent from a URL source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `source` | object |  |

## Native endpoint

Through the native Sendible API, this operation is `POST 0.2/tw/uploads` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-intent.md) for the provider-specific parameters and requirements.

