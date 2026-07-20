# BoardCRM: Create Deal

Creates a new deal in BoardCRM.

```
POST https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columnId` | number | no | Deal column ID. |
| `leadId` | number | no | Existing lead ID to attach to the deal. |
| `lead.name` | string | no | Name for a new lead created together with the deal. |
| `lead.email` | string | no | Email for a new lead created together with the deal. |
| `fields.title` | string | no | Title field value for the new deal. |
| `fields.description` | string | no | Description field value for the new deal. |
| `deadline` | string | no | Deal deadline in BoardCRM datetime format. |

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
      "lead": {},
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
| `lead` | object |  |
| `lead_id` | number |  |
| `reason_id` | number |  |
| `service_id` | string |  |
| `source` | string |  |
| `startline` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /offer/create` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

