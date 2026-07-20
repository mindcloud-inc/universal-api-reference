# Short.io: List Links

Retrieves links from Short.io.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-links?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-links?${params}`, {
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
| `domainId` | number | yes | Domain ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idString` | string | no | Link ID string. |
| `folderId` | string | no | Folder ID. |
| `createdAt` | string | no | Created-at selector. |
| `beforeDate` | string | no | Return links created before this timestamp. |
| `afterDate` | string | no | Return links created after this timestamp. |
| `dateSortOrder` | string | no | Sort order for link dates. |
| `pageToken` | string | no | Pagination token from a previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "cloaking": true,
      "createdAt": "string",
      "displayPath": "string",
      "domainId": 1,
      "hasPassword": true,
      "id": "string",
      "idString": "string",
      "originalURL": "https://example.com",
      "ownerId": 1,
      "path": "string",
      "secureShortURL": "https://example.com",
      "shortURL": "https://example.com",
      "skipQS": true,
      "source": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `cloaking` | boolean |  |
| `createdAt` | string |  |
| `displayPath` | string |  |
| `domainId` | number |  |
| `hasPassword` | boolean |  |
| `id` | string |  |
| `idString` | string |  |
| `originalURL` | string |  |
| `ownerId` | number |  |
| `path` | string |  |
| `secureShortURL` | string |  |
| `shortURL` | string |  |
| `skipQS` | boolean |  |
| `source` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Short.io API, this operation is `GET /api/links` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

