# Craftboxx: Update Article

Updates an article in Craftboxx.

```
PUT https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | number | yes | The Craftboxx article ID. |
| `currency` | string | no | The article currency. |
| `name` | string | no | The article name. |
| `unitPrice` | number | no | The article unit price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dangerous_material": true,
      "first_line": "string",
      "icon": "string",
      "id": 1,
      "interfaces": [
        "string"
      ],
      "name": "Ava Chen",
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "unit": "string",
      "unit_price": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vat_included": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Article color. |
| `created_at` | date | Creation timestamp. |
| `currency` | string | Currency code. |
| `dangerous_material` | boolean | Whether the article is dangerous material. |
| `first_line` | string | Primary display line. |
| `icon` | string | Article icon. |
| `id` | number | Article ID. |
| `interfaces` | array<string> | Available interface flags. |
| `name` | string | Article name. |
| `planner_changelog_url` | string | Planner changelog URL. |
| `planner_delete_url` | string | Planner delete URL. |
| `planner_details_url` | string | Planner details URL. |
| `planner_edit_url` | string | Planner edit URL. |
| `unit` | string | Unit code. |
| `unit_price` | number | Unit price. |
| `updated_at` | date | Update timestamp. |
| `vat_included` | string | VAT included flag. |

## Native endpoint

Through the native Craftboxx API, this operation is `PUT articles/:articleId` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

