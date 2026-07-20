# CustomGPT.ai: Update Document Metadata

Updates document metadata in a CustomGPT.ai agent.

```
PUT https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-document-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-document-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "pageId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-document-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "pageId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID of the agent. |
| `pageId` | number | yes | The document page ID. |
| `title` | string | yes | The updated document title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "image": "string",
      "pageId": 1,
      "title": "string",
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
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `image` | string |  |
| `pageId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `PUT /projects/:projectId/pages/:pageId/metadata` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-metadata.md) for the provider-specific parameters and requirements.

