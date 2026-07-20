# Coda: Create Doc

Creates a new doc in Coda.

```
POST https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-doc', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |
| `sourceDoc` | string | no |  |
| `timezone` | string | no |  |
| `folderId` | string | no |  |
| `initialPage` | object | no |  |
| `initialPage.name` | string | no |  |
| `initialPage.subtitle` | string | no |  |
| `initialPage.iconName` | string | no |  |
| `initialPage.imageUrl` | string | no |  |
| `initialPage.parentPageId` | string | no |  |
| `initialPage.pageContent` | object | no |  |
| `initialPage.pageContent.type` | string | no |  |
| `initialPage.pageContent.canvasContent` | object | no |  |
| `initialPage.pageContent.canvasContent.format` | string | no |  |
| `initialPage.pageContent.canvasContent.content` | string | no |  |
| `initialPage.pageContent.url` | string | no |  |
| `initialPage.pageContent.renderMethod` | string | no |  |
| `initialPage.pageContent.mode` | string | no |  |
| `initialPage.pageContent.includeSubpages` | boolean | no |  |
| `initialPage.pageContent.sourcePageId` | string | no |  |
| `initialPage.pageContent.sourceDocId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "requestId": "string",
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
| `requestId` | string |  |
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

Through the native Coda API, this operation is `POST /docs` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-doc.md) for the provider-specific parameters and requirements.

