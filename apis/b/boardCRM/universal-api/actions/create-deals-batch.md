# BoardCRM: Create Deals Batch

Creates multiple deal records in BoardCRM.

```
POST https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deals-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deals-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/create-deals-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offers[]` | array<object> | yes | Array of deal payloads using the BoardCRM create-deal shape. |

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
      "service_id": 1,
      "source": "string",
      "startline": 1,
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
| `service_id` | number |  |
| `source` | string |  |
| `startline` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native BoardCRM API, this operation is `POST /offer/create-some` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deals-batch.md) for the provider-specific parameters and requirements.

