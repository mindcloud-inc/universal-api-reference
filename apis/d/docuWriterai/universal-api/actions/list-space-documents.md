# DocuWriter.ai: List Space Documents



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-space-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-space-documents?connectionId=$CONNECTION_ID&spaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-space-documents?${params}`, {
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
| `spaceId` | number | yes | The ID of the Space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "parentId": 1,
      "spaceId": 1,
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | ISO-8601 timestamp when the document was created. |
| `id` | number | Document ID. |
| `name` | string | Document title. |
| `parentId` | number | Parent folder ID when nested. |
| `spaceId` | number | Containing Space ID. |
| `type` | number | Numeric document type returned by DocuWriter. |
| `updatedAt` | date | ISO-8601 timestamp when the document was last updated. |
| `url` | string | URL to view the document in DocuWriter. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `GET /api/spaces/{{space_id}}/documents` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-documents.md) for the provider-specific parameters and requirements.

