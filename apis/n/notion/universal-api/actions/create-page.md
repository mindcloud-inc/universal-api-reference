# Notion: Create Page

Creates a new page in Notion.

```
POST https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-page', {
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
| `parent` | object | no |  |
| `parent.pageId` | string | no |  |
| `properties` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent.databaseId` | string | no |  |
| `parent.dataSourceId` | string | no |  |
| `parent.workspace` | boolean | no |  |
| `children[]` | array<object> | no |  |
| `content[]` | array<object> | no |  |
| `markdown` | string | no |  |
| `icon` | object | no |  |
| `cover` | object | no |  |
| `template` | object | no |  |
| `template.type` | string | no |  |
| `template.templateId` | string | no |  |
| `position` | object | no |  |
| `position.type` | string | no |  |
| `position.afterBlock.id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "cover": {},
      "createdBy": {
        "id": "string",
        "object": "string"
      },
      "createdTime": "string",
      "icon": {},
      "id": "string",
      "inTrash": true,
      "isLocked": true,
      "lastEditedBy": {
        "id": "string",
        "object": "string"
      },
      "lastEditedTime": "string",
      "object": "string",
      "parent": {
        "type": "string",
        "workspace": true
      },
      "properties": {
        "title": {
          "id": "string",
          "type": "string"
        }
      },
      "publicUrl": {},
      "requestId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `cover` | object |  |
| `createdBy.id` | string |  |
| `createdBy.object` | string |  |
| `createdTime` | string |  |
| `icon` | object |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `isLocked` | boolean |  |
| `lastEditedBy.id` | string |  |
| `lastEditedBy.object` | string |  |
| `lastEditedTime` | string |  |
| `object` | string |  |
| `parent.type` | string |  |
| `parent.workspace` | boolean |  |
| `properties.title.id` | string |  |
| `properties.title.type` | string |  |
| `publicUrl` | object |  |
| `requestId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Notion API, this operation is `POST /pages` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

