# Webflow: List Pages

Retrieves a list of pages from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-pages?${params}`, {
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
| `siteId` | string | yes | Unique identifier for a Site. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localeId` | string | no | Unique identifier for a specific Locale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "branchId": "string",
      "canBranch": true,
      "collectionId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "id": "string",
      "isBranch": true,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "localeId": "string",
      "openGraph": {},
      "parentId": "string",
      "publishedPath": "string",
      "seo": {},
      "siteId": "string",
      "slug": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `branchId` | string |  |
| `canBranch` | boolean |  |
| `collectionId` | string |  |
| `createdOn` | date |  |
| `draft` | boolean |  |
| `id` | string |  |
| `isBranch` | boolean |  |
| `lastUpdated` | date |  |
| `localeId` | string |  |
| `openGraph` | object |  |
| `parentId` | string |  |
| `publishedPath` | string |  |
| `seo` | object |  |
| `siteId` | string |  |
| `slug` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Webflow API, this operation is `GET /sites/:site_id/pages` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

