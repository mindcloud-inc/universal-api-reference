# ZapCap: Upload Video by URL (Mapped Field)

Uploads a video to ZapCap from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url-mapped-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url-mapped-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/upload-video-by-url-mapped-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Publicly accessible MP4 URL to import into ZapCap. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "storageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Uploaded ZapCap video ID. |
| `status` | string | Upload status. |
| `storageId` | string | Storage identifier returned by ZapCap. |

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/url` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-video-by-url-mapped-field.md) for the provider-specific parameters and requirements.

