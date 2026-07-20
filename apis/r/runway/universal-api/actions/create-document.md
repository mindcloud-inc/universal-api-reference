# Runway: Create Document

Creates a document in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Markdown or plain text document content. |
| `name` | string | yes | Descriptive name for the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string",
      "usedBy": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `usedBy` | array<object> |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/documents` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

