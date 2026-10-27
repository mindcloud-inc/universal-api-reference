# Slack: Get File Upload URL



```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-upload-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "length": 1,
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-upload-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "length": 1,
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `length` | number | yes | Exact file size in bytes. |
| `filename` | string | yes | File name sent to Slack. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_id": "string",
      "ok": true,
      "upload_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_id` | string | Slack file ID to pass to Complete File Upload. |
| `ok` | boolean | Whether Slack issued an upload URL. |
| `upload_url` | string | One-time URL for uploading exact file bytes. |

## Native endpoint

Through the native Slack API, this operation is `POST files.getUploadURLExternal` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-upload-url.md) for the provider-specific parameters and requirements.

