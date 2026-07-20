# Webflow: Update Page Metadata

Updates metadata for a page in Webflow.

```
PUT https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/update-page-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | Unique identifier of the page. |
| `title` | string | no | Updated page title. |
| `slug` | string | no | Updated page slug. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `localeId` | string | no | Optional locale identifier for localized page metadata updates. |
| `seo` | object | no | SEO settings payload. |
| `openGraph` | object | no | Open Graph settings payload. |

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

Through the native Webflow API, this operation is `PUT /pages/:page_id` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-metadata.md) for the provider-specific parameters and requirements.

