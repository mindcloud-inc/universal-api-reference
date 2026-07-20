# Craftboxx: Get Article

Returns a specific article from Craftboxx.

```
GET https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/get-article?connectionId=$CONNECTION_ID&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/get-article?${params}`, {
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
| `articleId` | number | yes | The Craftboxx article ID. |

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

Through the native Craftboxx API, this operation is `GET articles/:articleId` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

