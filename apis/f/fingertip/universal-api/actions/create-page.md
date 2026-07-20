# Fingertip: Create Page



```
POST https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "slug": "string",
  "name": "Ava Chen",
  "bodySiteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "slug": "string",
    "name": "Ava Chen",
    "bodySiteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | yes | ID of the site to create a page in |
| `slug` | string | yes | URL-friendly path segment for the page |
| `name` | string | yes | Name of the page |
| `bodySiteId` | string | yes | ID of the site this page belongs to |
| `description` | string | no | Description of the page content |
| `position` | number | no | Display position of the page within the site |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": {
        "bannerMedia": {},
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "logoMedia": {},
        "name": "Ava Chen",
        "pageThemeId": "string",
        "position": 1,
        "siteId": "string",
        "slug": "string",
        "socialIcons": {},
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | object | The newly created page |
| `page.bannerMedia` | object |  |
| `page.createdAt` | date |  |
| `page.description` | string |  |
| `page.id` | string |  |
| `page.logoMedia` | object |  |
| `page.name` | string |  |
| `page.pageThemeId` | string |  |
| `page.position` | number |  |
| `page.siteId` | string |  |
| `page.slug` | string |  |
| `page.socialIcons` | object |  |
| `page.updatedAt` | date |  |

## Native endpoint

Through the native Fingertip API, this operation is `POST /v1/sites/:siteId/pages` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

