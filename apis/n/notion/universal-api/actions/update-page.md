# Notion: Update Page

Updates an existing page in Notion.

```
PUT https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "page_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "page_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page_id` | string | yes |  |
| `properties` | object | no |  |
| `archived` | boolean | no |  |
| `inTrash` | boolean | no |  |
| `isLocked` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eraseContent` | boolean | no |  |
| `icon` | object | no |  |
| `cover` | object | no |  |
| `template` | object | no |  |
| `template.type` | string | no |  |
| `template.templateId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "cover": {},
      "createdTime": "2026-05-07T12:00:00.000Z",
      "icon": {},
      "id": "string",
      "inTrash": true,
      "isLocked": true,
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "parent": {},
      "properties": {},
      "publicUrl": "https://example.com",
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
| `createdTime` | date |  |
| `icon` | object |  |
| `id` | string |  |
| `inTrash` | boolean |  |
| `isLocked` | boolean |  |
| `lastEditedTime` | date |  |
| `object` | string |  |
| `parent` | object |  |
| `properties` | object |  |
| `publicUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Notion API, this operation is `PATCH /pages/:page_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

