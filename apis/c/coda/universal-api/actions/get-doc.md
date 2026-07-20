# Coda: Get Doc

Retrieves details for a Coda doc.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-doc?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-doc?${params}`, {
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
| `docId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "docSize": {
        "baseTableCount": 1,
        "overApiSizeLimit": true,
        "pageCount": 1,
        "tableAndViewCount": 1,
        "totalRowCount": 1
      },
      "folder": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "folderId": "string",
      "href": "string",
      "icon": {
        "browserLink": "https://example.com",
        "name": "Ava Chen",
        "type": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "ownerName": "Ava Chen",
      "sourceDoc": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "type": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserLink` | string |  |
| `createdAt` | date |  |
| `docSize.baseTableCount` | number |  |
| `docSize.overApiSizeLimit` | boolean |  |
| `docSize.pageCount` | number |  |
| `docSize.tableAndViewCount` | number |  |
| `docSize.totalRowCount` | number |  |
| `folder.browserLink` | string |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `folder.type` | string |  |
| `folderId` | string |  |
| `href` | string |  |
| `icon.browserLink` | string |  |
| `icon.name` | string |  |
| `icon.type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `ownerName` | string |  |
| `sourceDoc.browserLink` | string |  |
| `sourceDoc.href` | string |  |
| `sourceDoc.id` | string |  |
| `sourceDoc.type` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `workspace.browserLink` | string |  |
| `workspace.id` | string |  |
| `workspace.name` | string |  |
| `workspace.type` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-doc.md) for the provider-specific parameters and requirements.

