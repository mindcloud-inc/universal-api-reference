# DocuWriter.ai: Update Space Document



```
PUT https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/update-space-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/update-space-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": "string",
  "spaceMenuItem": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/update-space-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": "string",
    "spaceMenuItem": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | New document body content. |
| `parentId` | number | no | Optional parent folder ID. |
| `space` | string | yes | ID or UUID of the Space. |
| `spaceMenuItem` | number | yes | ID of the document to update. |
| `title` | string | no | New document title. |
| `type` | string | no | Storage format: blank or markdown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "parentId": 1,
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
| `id` | number | Document ID. |
| `name` | string | Document title. |
| `parentId` | number | Parent folder ID when nested. |
| `type` | number | Document type. |
| `updatedAt` | date | ISO-8601 timestamp when the document was updated. |
| `url` | string | URL to the updated page in the app. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `PUT /api/spaces/{{space}}/documents/{{spaceMenuItem}}` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space-document.md) for the provider-specific parameters and requirements.

