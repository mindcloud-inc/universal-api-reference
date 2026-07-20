# SignRequest: Get Document Attachment



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document-attachment?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-document-attachment?${params}`, {
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
| `uuid` | string | yes |  |

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

Through the native SignRequest API, this operation is `GET /document-attachments/:uuid/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-attachment.md) for the provider-specific parameters and requirements.

