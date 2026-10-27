# Slack: Complete File Upload



```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/complete-file-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/complete-file-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "files[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/complete-file-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "files[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | yes | File IDs from Get File Upload URL, with optional titles. |
| `files[].id` | string | yes | The file_id returned by Get File Upload URL. |
| `channelId` | string | no | Channel where Slack should share the finalized file. Omit to keep private. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[].title` | string | no | Optional display title for this uploaded file. |
| `threadTs` | string | no | Parent message timestamp when sharing in a thread. |
| `initialComment` | string | no | Optional message introducing the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
        {
          "id": "string",
          "mimetype": "string",
          "name": "Ava Chen",
          "size": 1
        }
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `files` | array<object> | Finalized Slack files. |
| `files[].id` | string | Finalized Slack file ID. |
| `files[].mimetype` | string | Detected MIME type. |
| `files[].name` | string | Finalized file name. |
| `files[].size` | number | Finalized file size in bytes. |
| `ok` | boolean | Whether Slack finalized the upload. |

## Native endpoint

Through the native Slack API, this operation is `POST files.completeUploadExternal` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-file-upload.md) for the provider-specific parameters and requirements.

