# SignRequest: List Document Attachments



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-document-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-document-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-document-attachments?${params}`, {
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
| `documentUuid` | string | no |  |
| `documentExternalId` | string | no |  |
| `created` | string | no |  |

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

Through the native SignRequest API, this operation is `GET /document-attachments/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-document-attachments.md) for the provider-specific parameters and requirements.

