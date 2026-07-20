# Papyrs: Create Page



```
POST https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "json[]": [
    [
      "string"
    ]
  ],
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "json[]": [["string"]],
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | Optional folder path for the page. |
| `json[]` | array<array> | yes | The Papyrs page content JSON structure. |
| `layout[]` | array<array> | no | Optional page layout definition. |
| `notifications` | object | no | Optional notification settings keyed by user ID. |
| `permissions` | object | no | Optional permission settings keyed by user ID. |
| `title` | string | yes | The title of the new page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": "string",
      "is_public": true,
      "json": [
        [
          "string"
        ]
      ],
      "json[]": [
        {
          "classname": "Ava Chen",
          "html": "string",
          "id": "string",
          "text": "string"
        }
      ],
      "layout": [
        [
          "string"
        ]
      ],
      "notifications": {},
      "permissions": {},
      "slug": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Page category path. |
| `created_at` | date | Page creation timestamp. |
| `created_by` | string | Page creator display name. |
| `id` | string | Papyrs page ID. |
| `is_public` | boolean | Whether the page is public. |
| `json` | array<array> | Page content columns and widgets. |
| `json[][].classname` | string | Widget class name. |
| `json[][].html` | string | Rendered widget HTML. |
| `json[][].id` | string | Widget ID. |
| `json[][].text` | string | Plain-text widget content. |
| `layout` | array<array> | Page layout definition. |
| `notifications` | object | Notification settings keyed by user ID. |
| `permissions` | object | Permission settings keyed by user ID. |
| `slug` | string | Page slug. |
| `title` | string | Page title. |
| `updated_at` | date | Page update timestamp. |
| `url` | string | Absolute page URL. |

## Native endpoint

Through the native Papyrs API, this operation is `POST /pages/create/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

