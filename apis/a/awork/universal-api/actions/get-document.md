# Awork: Get Document

Retrieves a document from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | The id of the document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "currentDocumentVersionId": "string",
      "documentSpace": {
        "color": "string",
        "createdBy": "string",
        "createdOn": "2026-05-07T12:00:00.000Z",
        "emoji": "string",
        "id": "string",
        "name": "Ava Chen",
        "order": 1,
        "updatedBy": "string",
        "updatedOn": "2026-05-07T12:00:00.000Z",
        "workspaceAccessLevel": "string"
      },
      "documentSpaceId": "string",
      "emoji": "string",
      "id": "string",
      "isExternal": true,
      "isHiddenForConnectUsers": true,
      "isPrivate": true,
      "name": "Ava Chen",
      "order": 1,
      "rootDocumentCreatedBy": "string",
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `currentDocumentVersionId` | string |  |
| `documentSpace.color` | string |  |
| `documentSpace.createdBy` | string |  |
| `documentSpace.createdOn` | date |  |
| `documentSpace.emoji` | string |  |
| `documentSpace.id` | string |  |
| `documentSpace.name` | string |  |
| `documentSpace.order` | number |  |
| `documentSpace.updatedBy` | string |  |
| `documentSpace.updatedOn` | date |  |
| `documentSpace.workspaceAccessLevel` | string |  |
| `documentSpaceId` | string |  |
| `emoji` | string |  |
| `id` | string |  |
| `isExternal` | boolean |  |
| `isHiddenForConnectUsers` | boolean |  |
| `isPrivate` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `rootDocumentCreatedBy` | string |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Awork API, this operation is `GET /documents/:documentId` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

