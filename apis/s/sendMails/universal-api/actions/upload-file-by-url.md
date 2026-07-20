# SendMails: Upload File By Url

Uploads a file to SendMails from a URL.

```
POST https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/upload-file-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/upload-file-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendMails/latest/actions/upload-file-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | string | yes | JSON array string of file objects, each with a required url and optional subdirectory, as documented by SendMails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string | Source file URL that SendMails processed. |
| `message` | string | Provider result message for this file. |
| `status` | number | Provider success indicator for this file. |

## Native endpoint

Through the native SendMails API, this operation is `POST /file/upload` (base URL `https://app.sendmails.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-by-url.md) for the provider-specific parameters and requirements.

