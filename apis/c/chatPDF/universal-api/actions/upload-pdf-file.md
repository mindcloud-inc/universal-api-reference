# ChatPDF: Upload PDF File



```
POST https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/upload-pdf-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/upload-pdf-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/upload-pdf-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | PDF file to upload to ChatPDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sourceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sourceId` | string | ChatPDF source ID created from the file upload. |

## Native endpoint

Through the native ChatPDF API, this operation is `POST /sources/add-file` (base URL `https://api.chatpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-pdf-file.md) for the provider-specific parameters and requirements.

