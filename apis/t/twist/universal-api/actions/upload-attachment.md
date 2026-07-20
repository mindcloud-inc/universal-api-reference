# Twist: Upload Attachment

Uploads a new attachment to Twist.

```
POST https://connect.mindcloud.co/v1/universal/twist/latest/actions/upload-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twist/latest/actions/upload-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachmentId": "string",
  "file_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/upload-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachmentId": "string",
    "file_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentId` | string | yes | A UUID that will be the id of the attachment. |
| `file_name` | file | yes | Provide raw base64 file contents or a public file URL. Raw base64 should not include a data:...;base64, prefix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentId": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "title": "string",
      "underlyingType": "string",
      "uploadState": "string",
      "url": "https://example.com",
      "urlType": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentId` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `title` | string |  |
| `underlyingType` | string |  |
| `uploadState` | string |  |
| `url` | string |  |
| `urlType` | string |  |

## Native endpoint

Through the native Twist API, this operation is `POST /attachments/upload` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment.md) for the provider-specific parameters and requirements.

