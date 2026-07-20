# Makeswift: Update Page

Updates an existing page in Makeswift.

```
PUT https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageIdOrPathname": "Ava Chen",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageIdOrPathname": "Ava Chen",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageIdOrPathname` | string | yes | Page ID or pathname to update. |
| `siteId` | string | yes | The site ID containing the page. |
| `name` | string | no | Updated page name. |
| `isOnline` | boolean | no | Whether the page is online. |

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

Through the native Makeswift API, this operation is `PATCH /v6/pages/:pageIdOrPathname` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

