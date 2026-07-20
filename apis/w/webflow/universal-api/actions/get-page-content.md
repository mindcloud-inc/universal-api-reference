# Webflow: Get Page Content

Retrieves static page content from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-content?connectionId=$CONNECTION_ID&limit=25&offset=0&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/get-page-content?${params}`, {
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
      "branchId": "string",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "nodes": [
        {}
      ],
      "pageId": "string",
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | string | Branch ID when content is versioned. |
| `lastUpdated` | date | Last content update timestamp. |
| `nodes` | array<object> | Page content nodes. |
| `pageId` | string | Page ID for the content response. |
| `pagination` | object | Pagination metadata for nodes. |

## Native endpoint

Through the native Webflow API, this operation is `GET /pages/:page_id/dom` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-page-content.md) for the provider-specific parameters and requirements.

