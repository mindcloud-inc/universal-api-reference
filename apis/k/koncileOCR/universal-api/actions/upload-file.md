# Koncile OCR: Upload File



```
POST https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/upload-file', {
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
| `doc_id` | number | no | Complete an existing document by document ID. |
| `files` | file | yes | One file to upload for extraction. Koncile accepts PDF, PNG, and JPEG uploads on the files field. |
| `folder_id` | number | no | Store the uploaded document in this folder. |
| `metadata` | string | no | A JSON string with contextual extraction hints. |
| `template_id` | number | no | Extract data with this template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task_ids` | array<string> | Task identifiers returned for the uploaded file processing jobs. |

## Native endpoint

Through the native Koncile OCR API, this operation is `POST /upload_file` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

