# Kaiten: Update Card

Updates an existing card in Kaiten.

```
PUT https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/update-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | number | yes | The Kaiten card ID. |
| `title` | string | no | The card title. |
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
      "blocked": true,
      "blocking_card": true,
      "board_id": 1,
      "children_count": 1,
      "children_done": 1,
      "column_changed_at": "2026-05-07T12:00:00.000Z",
      "column_id": 1,
      "comment_last_added_at": "2026-05-07T12:00:00.000Z",
      "comments_total": 1,
      "completed_at": "2026-05-07T12:00:00.000Z",
      "completed_on_time": true,
      "condition": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "description_filled": true,
      "due_date": "2026-05-07T12:00:00.000Z",
      "due_date_time_present": true,
      "expires_later": true,
      "first_moved_to_in_progress_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "key": "string",
      "lane_changed_at": "2026-05-07T12:00:00.000Z",
      "lane_id": 1,
      "last_moved_at": "2026-05-07T12:00:00.000Z",
      "last_moved_to_done_at": "2026-05-07T12:00:00.000Z",
      "milestone_id": 1,
      "owner": {},
      "owner_id": 1,
      "parent_link_ids": [
        1
      ],
      "parents_count": 1,
      "public": true,
      "service_id": 1,
      "share_id": "string",
      "size": 1,
      "size_text": "string",
      "size_unit": "string",
      "sort_order": 1,
      "source": "string",
      "sprint_id": 1,
      "state": 1,
      "tag_ids": [
        1
      ],
      "title": "string",
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
| `blocked` | boolean | Blocked flag |
| `blocking_card` | boolean | Blocking card flag |
| `board_id` | number | Board ID |
| `children_count` | number | Child count |
| `children_done` | number | Completed child count |
| `column_changed_at` | date | Column changed timestamp |
| `column_id` | number | Column ID |
| `comment_last_added_at` | date | Last comment timestamp |
| `comments_total` | number | Comment count |
| `completed_at` | date | Completion timestamp |
| `completed_on_time` | boolean | Completion on time flag |
| `condition` | number | Condition code |
| `created` | date | Create timestamp |
| `description` | string | Card description |
| `description_filled` | boolean | Description present flag |
| `due_date` | date | Due date |
| `due_date_time_present` | boolean | Due date time present flag |
| `expires_later` | boolean | Expiry flag |
| `first_moved_to_in_progress_at` | date | First in-progress timestamp |
| `id` | number | Card ID |
| `key` | string | Card key |
| `lane_changed_at` | date | Lane changed timestamp |
| `lane_id` | number | Lane ID |
| `last_moved_at` | date | Last move timestamp |
| `last_moved_to_done_at` | date | Last done timestamp |
| `milestone_id` | number | Milestone ID |
| `owner` | object | Owner object |
| `owner_id` | number | Owner ID |
| `parent_link_ids` | array<number> | Parent link IDs |
| `parents_count` | number | Parent count |
| `public` | boolean | Public flag |
| `service_id` | number | Service ID |
| `share_id` | string | Share ID |
| `size` | number | Size value |
| `size_text` | string | Size text |
| `size_unit` | string | Size unit |
| `sort_order` | number | Card position |
| `source` | string | Source channel |
| `sprint_id` | number | Sprint ID |
| `state` | number | State code |
| `tag_ids` | array<number> | Tag IDs |
| `title` | string | Card title |
| `type_id` | number | Card type ID |
| `uid` | string | Card UID |
| `updated` | date | Update timestamp |
| `updater_id` | number | Updater user ID |
| `version` | number | Version counter |

## Native endpoint

Through the native Kaiten API, this operation is `PATCH /cards/:cardId` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-card.md) for the provider-specific parameters and requirements.

