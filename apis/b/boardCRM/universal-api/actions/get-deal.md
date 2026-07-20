# BoardCRM: Get Deal

Retrieves a single deal from BoardCRM.

```
GET https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoardCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/get-deal?${params}`, {
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
| `id` | number | yes | Deal ID. |

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

Through the native BoardCRM API, this operation is `POST /offer/get` (base URL `https://api.boardcrm.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

