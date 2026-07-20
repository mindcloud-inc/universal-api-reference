# The Guardian: Get Item

Retrieves a Guardian item by path.

```
GET https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Guardian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-item?connectionId=$CONNECTION_ID&itemPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemPath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-item?${params}`, {
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
| `itemPath` | string | yes | Guardian content path or item id, for example sport/2022/oct/07/example-story. |
| `showEditorsPicks` | string | no | When true, include editors' picks for the requested item path. |
| `showMostViewed` | string | no | When true, include most-viewed content for the requested path. |
| `showRelated` | string | no | When true, include related content items. |
| `showStoryPackage` | string | no | When true, include story-package content for the requested item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "edition": {
        "apiUrl": "https://example.com",
        "code": "string",
        "id": "string",
        "webTitle": "string",
        "webUrl": "https://example.com"
      },
      "id": "string",
      "results": [
        {}
      ],
      "section": {
        "apiUrl": "https://example.com",
        "id": "string",
        "webTitle": "string",
        "webUrl": "https://example.com"
      },
      "sectionId": "string",
      "sectionName": "Ava Chen",
      "type": "string",
      "webPublicationDate": "string",
      "webTitle": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `edition` | object |  |
| `edition.apiUrl` | string |  |
| `edition.code` | string |  |
| `edition.id` | string |  |
| `edition.webTitle` | string |  |
| `edition.webUrl` | string |  |
| `id` | string |  |
| `results` | array<object> |  |
| `section` | object |  |
| `section.apiUrl` | string |  |
| `section.id` | string |  |
| `section.webTitle` | string |  |
| `section.webUrl` | string |  |
| `sectionId` | string |  |
| `sectionName` | string |  |
| `type` | string |  |
| `webPublicationDate` | string |  |
| `webTitle` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native The Guardian API, this operation is `GET /{{itemPath}}` (base URL `https://content.guardianapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

