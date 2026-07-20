# Timetonic: Get Images Media Files And Documents From URL

Retrieves media files and documents from a URL in Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-images-media-files-and-documents-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-images-media-files-and-documents-from-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-images-media-files-and-documents-from-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "errorCode": "string",
      "errorMsg": "string",
      "req": "string",
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `errorCode` | string |  |
| `errorMsg` | string |  |
| `req` | string |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-images-media-files-and-documents-from-url.md) for the provider-specific parameters and requirements.

