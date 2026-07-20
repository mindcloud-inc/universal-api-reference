# Webflow: Get Page Metadata

Retrieves metadata for a page from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-metadata?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-metadata?${params}`, {
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
| `pageId` | string | yes | Unique identifier for a Page. |

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
| `archived` | boolean | Whether the page is archived. |
| `branchId` | string | Branch ID when applicable. |
| `canBranch` | boolean | Whether the page can branch. |
| `collectionId` | string | Collection page ID when applicable. |
| `createdOn` | date | Creation timestamp. |
| `draft` | boolean | Whether the page is a draft. |
| `id` | string | Page ID. |
| `isBranch` | boolean | Whether the page is a branch page. |
| `lastUpdated` | date | Last update timestamp. |
| `localeId` | string | Locale ID for the page. |
| `openGraph` | object | Open Graph metadata object. |
| `parentId` | string | Parent page ID when nested. |
| `publishedPath` | string | Published path for the page. |
| `seo` | object | SEO configuration object. |
| `siteId` | string | Site ID for the page. |
| `slug` | string | Page slug. |
| `title` | string | Page title. |

## Native endpoint

Through the native Webflow API, this operation is `GET /pages/:page_id` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-metadata.md) for the provider-specific parameters and requirements.

