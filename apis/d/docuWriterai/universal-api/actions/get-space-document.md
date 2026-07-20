# DocuWriter.ai: Get Space Document



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-space-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-space-document?connectionId=$CONNECTION_ID&space=1&spaceMenuItem=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "1",
  "spaceMenuItem": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/get-space-document?${params}`, {
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
| `space` | number | yes | ID of the Space to query. |
| `spaceMenuItem` | number | yes | ID of the document within the Space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isContentConvertedToBlock": true,
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
| `content` | string | Document content returned by DocuWriter. |
| `createdAt` | date | ISO-8601 timestamp when the document was created. |
| `id` | number | Document ID. |
| `isContentConvertedToBlock` | boolean | Whether the document content has been converted to blocks. |
| `name` | string | Document title. |
| `parentId` | number | Parent folder ID when nested. |
| `spaceId` | number | Containing Space ID. |
| `type` | number | Numeric document type returned by DocuWriter. |
| `updatedAt` | date | ISO-8601 timestamp when the document was last updated. |
| `url` | string | URL to view the document in DocuWriter. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `GET /api/spaces/{{space}}/documents/{{spaceMenuItem}}` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space-document.md) for the provider-specific parameters and requirements.

