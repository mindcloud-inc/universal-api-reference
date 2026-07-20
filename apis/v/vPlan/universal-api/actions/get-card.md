# vPlan: Get Card



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-card?connectionId=$CONNECTION_ID&collectionId=string&cardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string",
  "cardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-card?${params}`, {
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
| `collectionId` | string | yes |  |
| `cardId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "board_id": "string",
      "card_recurring_id": "string",
      "collection_id": "string",
      "completed_at": "string",
      "created_at": "string",
      "custom_fields": [
        {}
      ],
      "date": "string",
      "days_active": 1,
      "days_diff": 1,
      "deleted_at": "string",
      "description": "string",
      "end": "string",
      "end_date": "string",
      "end_time": "string",
      "external_ref": "string",
      "id": "string",
      "locked": true,
      "name": "Ava Chen",
      "parent_card_id": "string",
      "position": 1,
      "rank": "string",
      "stage_id": "string",
      "start": "string",
      "start_date": "string",
      "start_time": "string",
      "status_id": "string",
      "time_tracking_running": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string | Batch identifier. |
| `board_id` | string | Board identifier. |
| `card_recurring_id` | string | Recurring card identifier. |
| `collection_id` | string | Collection identifier. |
| `completed_at` | string | Completion timestamp. |
| `created_at` | string | Creation timestamp. |
| `custom_fields` | array<object> | Custom field values. |
| `date` | string | Card date. |
| `days_active` | number | Active day count. |
| `days_diff` | number | Days difference metric. |
| `deleted_at` | string | Deletion timestamp. |
| `description` | string | Card description. |
| `end` | string | End datetime. |
| `end_date` | string | End date. |
| `end_time` | string | End time. |
| `external_ref` | string | External reference. |
| `id` | string | Card identifier. |
| `locked` | boolean | Whether the card is locked. |
| `name` | string | Card name. |
| `parent_card_id` | string | Parent card identifier. |
| `position` | number | Card position. |
| `rank` | string | Card rank. |
| `stage_id` | string | Stage identifier. |
| `start` | string | Start datetime. |
| `start_date` | string | Start date. |
| `start_time` | string | Start time. |
| `status_id` | string | Status identifier. |
| `time_tracking_running` | boolean | Whether time tracking is running. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `GET /collection/[:collection_id]/card/[:card_id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card.md) for the provider-specific parameters and requirements.

