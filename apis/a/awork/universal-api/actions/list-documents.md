# Awork: List Documents

Retrieves documents from Awork.

```
GET https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Awork `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Awork API, this operation is `GET /documents` (base URL `https://api.awork.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

