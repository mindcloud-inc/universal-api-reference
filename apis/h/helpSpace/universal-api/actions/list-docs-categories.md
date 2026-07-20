# HelpSpace: List Docs Categories

Retrieves docs categories from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-categories?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "docsSiteId": 1,
      "id": 1,
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "localeDefault": "string",
      "localesEnabled": [
        "string"
      ],
      "localized": [
        {}
      ],
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `docsSiteId` | number |  |
| `id` | number |  |
| `lastModifiedAt` | date |  |
| `localeDefault` | string |  |
| `localesEnabled` | array<string> |  |
| `localized` | array<object> |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /docs/categories` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-docs-categories.md) for the provider-specific parameters and requirements.

