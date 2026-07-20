# Foreplay: List Board Brands

Retrieves brands from a specific Foreplay board.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/list-board-brands?${params}`, {
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
| `boardId` | string | no | The ID of the board to retrieve brands from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_library_id": "string",
      "avatar": "string",
      "category": "string",
      "description": {
        "text": "string"
      },
      "id": "string",
      "is_delegate_page_with_linked_primary_profile": true,
      "name": "Ava Chen",
      "url": "https://example.com",
      "verification_status": "string",
      "websites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_library_id` | string |  |
| `avatar` | string |  |
| `category` | string |  |
| `description.text` | string |  |
| `id` | string |  |
| `is_delegate_page_with_linked_primary_profile` | boolean |  |
| `name` | string |  |
| `url` | string |  |
| `verification_status` | string |  |
| `websites[]` | string |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/board/brands` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-brands.md) for the provider-specific parameters and requirements.

