# SignRequest: Create Document Attachment



```
POST https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-document-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes |  |
| `fileFromUrl` | string | no |  |
| `fileFromContent` | string | no |  |
| `fileFromContentName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": "string",
      "file": "string",
      "fileFromUrl": "https://example.com",
      "name": "Ava Chen",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document` | string |  |
| `file` | string |  |
| `fileFromUrl` | string |  |
| `name` | string |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `POST /document-attachments/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-attachment.md) for the provider-specific parameters and requirements.

