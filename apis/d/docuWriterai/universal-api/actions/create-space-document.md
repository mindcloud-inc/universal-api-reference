# DocuWriter.ai: Create Space Document



```
POST https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "space": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "space": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Document body content. |
| `parentId` | number | no | Optional parent folder ID. |
| `path` | string | no | Slash-delimited folder path. |
| `space` | number | yes | ID of the Space. |
| `title` | string | yes | Document title. |
| `type` | string | no | Storage format: blank or markdown. |

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
      "type": 1,
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
| `type` | number | Document type. |
| `url` | string | URL to the new page in the app. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/spaces/{{space}}/documents` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space-document.md) for the provider-specific parameters and requirements.

