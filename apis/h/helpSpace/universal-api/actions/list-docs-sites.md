# HelpSpace: List Docs Sites

Retrieves docs sites from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-sites?${params}`, {
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
      "id": 1,
      "isMultiLingual": 1,
      "isPublic": 1,
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "localeDefault": "string",
      "localesEnabled": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | number |  |
| `isMultiLingual` | number |  |
| `isPublic` | number |  |
| `lastModifiedAt` | date |  |
| `localeDefault` | string |  |
| `localesEnabled` | array<string> |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /docs/sites` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-docs-sites.md) for the provider-specific parameters and requirements.

