# Filestack: Store File From URL

Creates a new file in Filestack from a URL.

```
POST https://connect.mindcloud.co/v1/universal/filestack/latest/actions/store-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestack/latest/actions/store-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://assets.filestackapi.com/watermark.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestack/latest/actions/store-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://assets.filestackapi.com/watermark.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | no | Optional filename to store in Filestack. Example: `watermark.png`. |
| `url` | string | yes | Public URL of the file to import into Filestack. Default: `https://assets.filestackapi.com/watermark.png`. Example: `https://assets.filestackapi.com/watermark.png`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mimeType` | string | no | Optional MIME type override, for example image/png. Example: `image/png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "key": "string",
      "size": 1,
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
| `filename` | string | The stored filename. |
| `key` | string | The storage key returned by Filestack. |
| `size` | number | The stored file size in bytes. |
| `type` | string | The stored file MIME type. |
| `url` | string | The Filestack CDN URL for the stored file. |

## Native endpoint

Through the native Filestack API, this operation is `POST /store/S3` (base URL `https://www.filestackapi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-file-from-url.md) for the provider-specific parameters and requirements.

