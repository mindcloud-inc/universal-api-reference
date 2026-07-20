# Kaiten: Create Card

Creates a card in Kaiten.

```
POST https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "boardId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "boardId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The card title. |
| `boardId` | number | yes | The Kaiten board ID. |
| `columnId` | number | no | The target column ID. |
| `laneId` | number | no | The target lane ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "asap": true,
      "board_id": 1,
      "children_count": 1,
      "children_done": 1,
      "column_id": 1,
      "comment_last_added_at": "2026-05-07T12:00:00.000Z",
      "comments_total": 1,
      "condition": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "description_filled": true,
      "due_date": "2026-05-07T12:00:00.000Z",
      "expires_later": true,
      "fifo_order": 1,
      "id": 1,
      "key": "string",
      "lane_id": 1,
      "owner": {},
      "owner_id": 1,
      "parents_count": 1,
      "sort_order": 1,
      "source": "string",
      "state": 1,
      "tag_ids": [
        1
      ],
      "title": "string",
      "type": {},
      "type_id": 1,
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updater_id": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Archive flag |
| `asap` | boolean | ASAP flag |
| `board_id` | number | Board ID |
| `children_count` | number | Child count |
| `children_done` | number | Completed child count |
| `column_id` | number | Column ID |
| `comment_last_added_at` | date | Last comment timestamp |
| `comments_total` | number | Comment count |
| `condition` | number | Condition code |
| `created` | date | Create timestamp |
| `description` | string | Card description |
| `description_filled` | boolean | Description present flag |
| `due_date` | date | Due date |
| `expires_later` | boolean | Expiry flag |
| `fifo_order` | number | FIFO position |
| `id` | number | Card ID |
| `key` | string | Card key |
| `lane_id` | number | Lane ID |
| `owner` | object | Owner object |
| `owner_id` | number | Owner ID |
| `parents_count` | number | Parent count |
| `sort_order` | number | Card position |
| `source` | string | Source channel |
| `state` | number | State code |
| `tag_ids` | array<number> | Tag IDs |
| `title` | string | Card title |
| `type` | object | Card type object |
| `type_id` | number | Card type ID |
| `uid` | string | Card UID |
| `updated` | date | Update timestamp |
| `updater_id` | number | Updater user ID |
| `version` | number | Version counter |

## Native endpoint

Through the native Kaiten API, this operation is `POST /cards` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

