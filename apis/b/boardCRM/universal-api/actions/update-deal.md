# BoardCRM: Update Deal

Updates an existing deal in BoardCRM.

```
PUT https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Deal ID. |
| `columnId` | number | no | Target column ID. |
| `reasonId` | number | no | Reason ID for a closed deal. |
| `deadline` | string | no | Deal deadline in BoardCRM datetime format. |
| `deadlineDone` | string | no | Deadline completion flag. |
| `lead.name` | string | no | Updated lead name. |
| `lead.email` | string | no | Updated lead email. |
| `fields.title` | string | no | Updated deal title. |
| `fields.description` | string | no | Updated deal description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "column_id": 1,
      "comment_cnt": 1,
      "created_at": "string",
      "deadline": "string",
      "deadline_done": true,
      "deadline_status": "string",
      "finished_at": "string",
      "id": 1,
      "lead_id": 1,
      "reason_id": 1,
      "service_id": "string",
      "source": "string",
      "startline": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `column_id` | number |  |
| `comment_cnt` | number |  |
| `created_at` | string |  |
| `deadline` | string |  |
| `deadline_done` | boolean |  |
| `deadline_status` | string |  |
| `finished_at` | string |  |
| `id` | number |  |
| `lead_id` | number |  |
| `reason_id` | number |  |
| `service_id` | string |  |
| `source` | string |  |
| `startline` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /offer/update` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

