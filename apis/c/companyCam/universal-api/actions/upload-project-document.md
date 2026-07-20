# CompanyCam: Upload Project Document

Upload a document to a CompanyCam project.

```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/upload-project-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/upload-project-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/upload-project-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document.name` | string | no | Example: `test.txt`. |
| `projectId` | string | yes |  |
| `document` | object | no |  |
| `document.attachment` | file | no | Base64 encoded file contents with 30 MB limit |

## Response

```json
{
  "success": true,
  "data": [
    {
      "byteSize": 1,
      "companyId": "string",
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
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
| `byteSize` | number |  |
| `companyId` | string |  |
| `contentType` | string |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `POST projects/:projectId/documents` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-project-document.md) for the provider-specific parameters and requirements.

