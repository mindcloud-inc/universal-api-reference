# OneDeck: Upload Record Attachment

Uploads an attachment to a OneDeck board record.

```
POST https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/upload-record-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/upload-record-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
  "recordId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
  "fileName": "sample.txt",
  "contentType": "text/plain",
  "fileContent": "Hello from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/upload-record-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "1ff5d564-2ea6-4053-8c20-fac2ef32f059",
    "recordId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
    "fileName": "sample.txt",
    "contentType": "text/plain",
    "fileContent": "Hello from MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | The OneDeck board ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f059`. |
| `recordId` | string | yes | The OneDeck record ID. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f029`. |
| `fileName` | string | yes | The file name to send in the x-file-name header. Example: `sample.txt`. |
| `contentType` | string | yes | The MIME type for the attachment. Example: `text/plain`. |
| `fileContent` | string | yes | Raw text content to upload as the attachment body. Example: `Hello from MindCloud`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `POST /boards/{{boardId}}/records/{{recordId}}/attachments` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-record-attachment.md) for the provider-specific parameters and requirements.

