# Notion: Retrieve Page

Retrieves details for a page from Notion.

```
GET https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page?connectionId=$CONNECTION_ID&page_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-page?${params}`, {
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
| `page_id` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterProperties[]` | array<string> | no |  |

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

Through the native Notion API, this operation is `GET /pages/:page_id` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-page.md) for the provider-specific parameters and requirements.

