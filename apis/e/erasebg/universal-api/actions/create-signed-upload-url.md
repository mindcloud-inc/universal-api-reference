# Erase.bg: Create Signed Upload URL

Creates a signed upload URL in Erase.bg.

```
POST https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/create-signed-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/create-signed-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/create-signed-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | File format or extension. |
| `name` | string | no | Desired asset name. |
| `path` | string | no | Destination folder path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "s3PresignedUrl": {
        "fields": {},
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `s3PresignedUrl` | object |  |
| `s3PresignedUrl.fields` | object |  |
| `s3PresignedUrl.url` | string |  |

## Native endpoint

Through the native Erase.bg API, this operation is `POST /service/platform/assets/v1.0/upload/signed-url` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signed-upload-url.md) for the provider-specific parameters and requirements.

