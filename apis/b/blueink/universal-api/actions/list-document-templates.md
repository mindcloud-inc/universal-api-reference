# Blueink: List Document Templates

Retrieves available document templates from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-document-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-document-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-document-templates?${params}`, {
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
      "fields": [
        {
          "defaultValue": "string",
          "editorRoles": [
            "string"
          ],
          "format": "string",
          "h": 1,
          "key": "string",
          "kind": "string",
          "label": "string",
          "page": 1,
          "vMax": 1,
          "vMin": 1,
          "vPattern": "string",
          "w": 1,
          "x": 1,
          "y": 1
        }
      ],
      "fileUrl": "https://example.com",
      "id": "string",
      "isShared": true,
      "name": "Ava Chen",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].defaultValue` | string |  |
| `fields[].editorRoles[]` | string |  |
| `fields[].format` | string |  |
| `fields[].h` | number |  |
| `fields[].key` | string |  |
| `fields[].kind` | string |  |
| `fields[].label` | string |  |
| `fields[].page` | number |  |
| `fields[].vMax` | number |  |
| `fields[].vMin` | number |  |
| `fields[].vPattern` | string |  |
| `fields[].w` | number |  |
| `fields[].x` | number |  |
| `fields[].y` | number |  |
| `fileUrl` | string |  |
| `id` | string |  |
| `isShared` | boolean |  |
| `name` | string |  |
| `roles[]` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /templates/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-document-templates.md) for the provider-specific parameters and requirements.

