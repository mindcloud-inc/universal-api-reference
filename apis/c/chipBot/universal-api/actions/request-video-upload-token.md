# ChipBot: Request Video Upload Token



```
POST https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-upload-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-upload-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checksumMd5": "string",
  "size": 1,
  "videoExpId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/request-video-upload-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checksumMd5": "string",
    "size": 1,
    "videoExpId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checksumMd5` | string | yes | MD5 checksum of the full video file. |
| `size` | number | yes | Video file size in bytes. |
| `videoExpId` | string | yes | The target video experience identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Upload-request result payload. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `POST /api/v2/utility/video-upload/request` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-video-upload-token.md) for the provider-specific parameters and requirements.

