# Canva: List Folder Items

Retrieves items in a Canva folder.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-folder-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-folder-items?connectionId=$CONNECTION_ID&folderId=root" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "root"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/list-folder-items?${params}`, {
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
| `folderId` | string | yes | Example: `root`. |
| `itemTypes` | list<string> | no | One of: `design`, `folder`, `image`. Accepts multiple values in one string, delimited by `,`. |
| `sortBy` | list | no | One of: `created_ascending`, `created_descending`, `modified_ascending`, `modified_descending`, `title_ascending`, `title_descending`. |
| `pinStatus` | list | no | One of: `any`, `pinned`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `continuation` | string | no | Example: `cursor_token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "design": {
            "createdAt": 1,
            "id": "string",
            "pageCount": 1,
            "title": "string",
            "updatedAt": 1,
            "urls": {
              "editUrl": "https://example.com",
              "viewUrl": "https://example.com"
            }
          },
          "folder": {
            "id": "string",
            "name": "Ava Chen"
          },
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].design` | object |  |
| `items[].design.createdAt` | number |  |
| `items[].design.id` | string |  |
| `items[].design.pageCount` | number |  |
| `items[].design.title` | string |  |
| `items[].design.updatedAt` | number |  |
| `items[].design.urls` | object |  |
| `items[].design.urls.editUrl` | string |  |
| `items[].design.urls.viewUrl` | string |  |
| `items[].folder` | object | Folder item payload when the list entry represents a folder. |
| `items[].folder.id` | string | Folder item ID. |
| `items[].folder.name` | string | Folder item name. |
| `items[].type` | string |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/folders/:folderId/items` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-items.md) for the provider-specific parameters and requirements.

