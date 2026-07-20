# Makeswift: List Pages

Retrieves pages for a site from Makeswift.

```
GET https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-pages?${params}`, {
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
| `siteId` | string | yes | The site ID to list pages from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of pages to return (1-100). Default: `20`. |
| `startingAfter` | string | no | Pagination cursor ID. |
| `locale` | string | no | Filter pages by locale. |
| `pathPrefix` | string | no | Filter pages by pathname prefix. |
| `includeOffline` | boolean | no | Include offline pages when true. |
| `sortBy` | string | no | Sort field. |
| `sortDirection` | string | no | Sort direction. |
| `versionRef` | string | no | Use this version reference for content reads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `hasMore` | boolean |  |
| `object` | string |  |

## Native endpoint

Through the native Makeswift API, this operation is `GET /v6/pages` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

