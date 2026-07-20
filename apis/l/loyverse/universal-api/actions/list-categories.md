# Loyverse: List Categories

Retrieves category records from the Loyverse catalog.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-categories?${params}`, {
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
| `categoriesIds` | string | no | Return only categories specified by a comma-separated list of IDs |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |
| `showDeleted` | boolean | no | Show deleted modifiers and modifier options |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {
          "color": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "deletedAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `categories[].color` | string |  |
| `categories[].createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `categories[].deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `categories[].id` | string | The category id. If included in the POST request it will cause an update instead of a creating a new object. |
| `categories[].name` | string |  |

## Native endpoint

Through the native Loyverse API, this operation is `GET /categories` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

