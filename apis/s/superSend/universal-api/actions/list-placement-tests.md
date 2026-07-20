# SuperSend: List Placement Tests

Retrieves placement tests from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-placement-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-placement-tests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-placement-tests?${params}`, {
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
| `teamId` | string | no |  |
| `senderId` | string | no |  |
| `status` | string | no | Allowed values: pending, sending, sent, completed, failed. |
| `search` | string | no |  |
| `conditionalFilters` | string | no | JSON string for score/date filters |
| `sortBy` | string | no | Allowed values: created_at, name, status, score, sent_at, completed_at. Default: created_at. |
| `sortOrder` | string | no | Allowed values: asc, desc. Default: desc. |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_send": true,
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "credit_cost": 1,
      "id": "string",
      "is_auto_test": true,
      "name": "Ava Chen",
      "object": "string",
      "results_summary": {
        "bounced": 1,
        "inbox": 1,
        "not_received": 1,
        "spam": 1
      },
      "score": 1,
      "sender": {
        "email": "ava@example.com",
        "id": "string",
        "provider": "string"
      },
      "sent_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "total_seeds": 1,
      "tracking_code": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_send` | boolean |  |
| `completed_at` | date |  |
| `created_at` | date |  |
| `created_by.email` | string |  |
| `created_by.id` | string |  |
| `created_by.name` | string |  |
| `credit_cost` | number |  |
| `id` | string |  |
| `is_auto_test` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `results_summary.bounced` | number |  |
| `results_summary.inbox` | number |  |
| `results_summary.not_received` | number |  |
| `results_summary.spam` | number |  |
| `score` | number |  |
| `sender.email` | string |  |
| `sender.id` | string |  |
| `sender.provider` | string |  |
| `sent_at` | date |  |
| `status` | string |  |
| `total_seeds` | number |  |
| `tracking_code` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /placement-tests` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-placement-tests.md) for the provider-specific parameters and requirements.

