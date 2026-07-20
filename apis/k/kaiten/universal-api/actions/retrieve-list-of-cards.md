# Kaiten: Retrieve List of Cards

Retrieves cards from Kaiten.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-cards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-cards?${params}`, {
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
| `boardId` | number | no | Filter cards by board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "asap": true,
      "board_id": 1,
      "board": {
        "id": 1,
        "title": "string"
      },
      "column_id": 1,
      "column": {
        "id": 1,
        "title": "string"
      },
      "comments_total": 1,
      "condition": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "files": [
        {
          "url": "https://example.com"
        }
      ],
      "id": 1,
      "lane_id": 1,
      "lane": {
        "id": 1,
        "title": "string"
      },
      "members": [
        {
          "id": 1
        }
      ],
      "owner_id": 1,
      "owner": {
        "full_name": "Ava Chen",
        "id": 1
      },
      "sort_order": 1,
      "source": "string",
      "state": 1,
      "tags": [
        {
          "id": 1
        }
      ],
      "title": "string",
      "type_id": 1,
      "type": {
        "id": 1,
        "name": "Ava Chen"
      },
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `asap` | boolean |  |
| `board_id` | number |  |
| `board.id` | number |  |
| `board.title` | string |  |
| `column_id` | number |  |
| `column.id` | number |  |
| `column.title` | string |  |
| `comments_total` | number |  |
| `condition` | number |  |
| `created` | date |  |
| `description` | string |  |
| `due_date` | date |  |
| `files[].url` | string |  |
| `id` | number |  |
| `lane_id` | number |  |
| `lane.id` | number |  |
| `lane.title` | string |  |
| `members[].id` | number |  |
| `owner_id` | number |  |
| `owner.full_name` | string |  |
| `owner.id` | number |  |
| `sort_order` | number |  |
| `source` | string |  |
| `state` | number |  |
| `tags[].id` | number |  |
| `title` | string |  |
| `type_id` | number |  |
| `type.id` | number |  |
| `type.name` | string |  |
| `uid` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /cards` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/retrieve-list-of-cards.md) for the provider-specific parameters and requirements.

