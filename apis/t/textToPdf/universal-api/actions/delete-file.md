# Text to pdf: Delete File

Deletes a file from Text to PDF by file ID.

```
DELETE https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Text to pdf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-file?connectionId=$CONNECTION_ID&arguments=%5Bobject%20Object%5D&arguments.fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arguments": "[object Object]",
  "arguments.fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/delete-file?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `arguments` | object | yes | Tool input arguments object. |
| `arguments.fileId` | string | yes | Unique file id to delete from temporary storage. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "message": "string",
        "success": true
      },
      "error": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.message` | string | File deletion status message. |
| `data.success` | boolean | Whether the file deletion succeeded. |
| `error` | string | Error message when execution fails. |
| `successful` | boolean | Whether the Composio tool execution succeeded. |

## Native endpoint

Through the native Text to pdf API, this operation is `POST /tools/execute/TEXT_TO_PDF_DELETE_FILE` (base URL `https://backend.composio.dev/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

