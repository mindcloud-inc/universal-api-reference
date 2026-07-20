# Certs 365: Upload Media File

Uploads a media file to Certs 365 storage.

```
POST https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-media-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certs365/latest/actions/upload-media-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Media file to upload to S3. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/upload` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-media-file.md) for the provider-specific parameters and requirements.

