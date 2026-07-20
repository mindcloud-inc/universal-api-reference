# Metance: List Files

Retrieves files from the current Metance workspace.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/list-files?${params}`, {
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
      "fileName": "Ava Chen",
      "fileOriginalName": "Ava Chen",
      "fileSize": 1,
      "fileType": 1,
      "id": 1,
      "s3Url": "https://example.com",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string | Internal file name |
| `fileOriginalName` | string | Original uploaded file name |
| `fileSize` | number | File size in bytes |
| `fileType` | number | File type code |
| `id` | number | File ID |
| `s3Url` | string | File URL |
| `status` | number | File status |

## Native endpoint

Through the native Metance API, this operation is `GET /file/list` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

