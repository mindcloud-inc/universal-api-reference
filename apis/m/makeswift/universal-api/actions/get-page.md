# Makeswift: Get Page

Retrieves a page from Makeswift.

```
GET https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-page?connectionId=$CONNECTION_ID&pageIdOrPathname=Ava%20Chen&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageIdOrPathname": "Ava Chen",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-page?${params}`, {
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
| `pageIdOrPathname` | string | yes | Page ID or pathname. |
| `siteId` | string | yes | The site ID containing the page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Read page data for a specific locale. |
| `versionRef` | string | no | Version reference for preview/published content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonicalUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "excludedFromSearchEngines": true,
      "id": "string",
      "isOnline": true,
      "locale": "string",
      "localizations": [
        {}
      ],
      "object": "string",
      "pathname": "Ava Chen",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "sitemapFrequency": "string",
      "sitemapPriority": 1,
      "socialImageUrl": "https://example.com",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonicalUrl` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `excludedFromSearchEngines` | boolean |  |
| `id` | string |  |
| `isOnline` | boolean |  |
| `locale` | string |  |
| `localizations` | array<object> |  |
| `object` | string |  |
| `pathname` | string |  |
| `publishedAt` | date |  |
| `sitemapFrequency` | string |  |
| `sitemapPriority` | number |  |
| `socialImageUrl` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Makeswift API, this operation is `GET /v6/pages/:pageIdOrPathname` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

