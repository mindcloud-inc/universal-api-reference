# Typeform: Upload a Video File



```
POST https://connect.mindcloud.co/v1/universal/typeform/latest/actions/upload-a-video-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/upload-a-video-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/upload-a-video-file', {
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
| `fieldId` | string | no | Field identifier for the video upload. |
| `formId` | string | no | Form identifier for the video upload. |
| `language` | string | no | Language code for the media asset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created video media ID. |
| `uploadUrl` | string | Temporary signed URL for uploading the video. |

## Native endpoint

Through the native Typeform API, this operation is `POST /media/videos` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-a-video-file.md) for the provider-specific parameters and requirements.

