# Content Snare: Get Request

Retrieves a request from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-request?${params}`, {
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
| `id` | string | yes | Request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved_fields_count": 1,
      "author_name": "Ava Chen",
      "board_column_id": "string",
      "board_column_sorting_position": "string",
      "clients": [
        {
          "avatar": "string",
          "company_name": "Ava Chen",
          "email": "ava@example.com",
          "full_name": "Ava Chen",
          "id": "string",
          "phone": "string",
          "url": "https://example.com"
        }
      ],
      "comments_enabled": true,
      "communications_template_name": "Ava Chen",
      "completion_percentage": 1,
      "country_code": "string",
      "done_fields_count": 1,
      "due": "2026-05-07T12:00:00.000Z",
      "fields_count": 1,
      "folder_name": "Ava Chen",
      "has_comments": true,
      "id": "string",
      "instruction_text": "string",
      "language_code": "string",
      "name": "Ava Chen",
      "owner_id": "string",
      "owner_name": "Ava Chen",
      "pages": [
        {
          "approved_fields_count": 1,
          "done_fields_count": 1,
          "fields_count": 1,
          "id": "string",
          "instruction_text": "string",
          "is_approved": true,
          "is_done": true,
          "name": "Ava Chen",
          "redo_fields_count": 1,
          "show_instruction": true,
          "sorting_position": 1
        }
      ],
      "passcode_enabled": true,
      "primary_client_id": "string",
      "redo_fields_count": 1,
      "request_template_name": "Ava Chen",
      "share_link": "https://example.com",
      "share_via_link_enabled": true,
      "show_instruction": true,
      "status": "string",
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
| `approved_fields_count` | number |  |
| `author_name` | string |  |
| `board_column_id` | string |  |
| `board_column_sorting_position` | string |  |
| `clients[].avatar` | string |  |
| `clients[].company_name` | string |  |
| `clients[].email` | string |  |
| `clients[].full_name` | string |  |
| `clients[].id` | string |  |
| `clients[].phone` | string |  |
| `clients[].url` | string |  |
| `comments_enabled` | boolean |  |
| `communications_template_name` | string |  |
| `completion_percentage` | number |  |
| `country_code` | string |  |
| `done_fields_count` | number |  |
| `due` | date |  |
| `fields_count` | number |  |
| `folder_name` | string |  |
| `has_comments` | boolean |  |
| `id` | string |  |
| `instruction_text` | string |  |
| `language_code` | string |  |
| `name` | string |  |
| `owner_id` | string |  |
| `owner_name` | string |  |
| `pages[].approved_fields_count` | number |  |
| `pages[].done_fields_count` | number |  |
| `pages[].fields_count` | number |  |
| `pages[].id` | string |  |
| `pages[].instruction_text` | string |  |
| `pages[].is_approved` | boolean |  |
| `pages[].is_done` | boolean |  |
| `pages[].name` | string |  |
| `pages[].redo_fields_count` | number |  |
| `pages[].show_instruction` | boolean |  |
| `pages[].sorting_position` | number |  |
| `passcode_enabled` | boolean |  |
| `primary_client_id` | string |  |
| `redo_fields_count` | number |  |
| `request_template_name` | string |  |
| `share_link` | string |  |
| `share_via_link_enabled` | boolean |  |
| `show_instruction` | boolean |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `GET /partner_api/v1/requests/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request.md) for the provider-specific parameters and requirements.

