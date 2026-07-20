# SuperSend: Get Placement Test

Retrieves a placement test from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-placement-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-placement-test?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-placement-test?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |

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
      "name": "Ava Chen",
      "object": "string",
      "placement_results": [
        {
          "check_attempts": 1,
          "checked_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "metadata": {},
          "placement": "string",
          "received_at": "2026-05-07T12:00:00.000Z",
          "seed_email": "ava@example.com",
          "tags": [
            [
              "string"
            ]
          ]
        }
      ],
      "results_summary": {
        "bounced": 1,
        "inbox": 1,
        "not_received": 1,
        "spam": 1
      },
      "score": 1,
      "seed_addresses": [
        {
          "email": "ava@example.com"
        }
      ],
      "sender": {
        "email": "ava@example.com",
        "id": "string",
        "provider": "string"
      },
      "sent_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "test_email_body": "ava@example.com",
      "test_email_from": "ava@example.com",
      "test_email_subject": "ava@example.com",
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
| `name` | string |  |
| `object` | string |  |
| `placement_results[].check_attempts` | number |  |
| `placement_results[].checked_at` | date |  |
| `placement_results[].id` | string |  |
| `placement_results[].metadata` | object |  |
| `placement_results[].placement` | string |  |
| `placement_results[].received_at` | date |  |
| `placement_results[].seed_email` | string |  |
| `placement_results[].tags[]` | array<string> |  |
| `results_summary.bounced` | number |  |
| `results_summary.inbox` | number |  |
| `results_summary.not_received` | number |  |
| `results_summary.spam` | number |  |
| `score` | number |  |
| `seed_addresses[].email` | string |  |
| `sender.email` | string |  |
| `sender.id` | string |  |
| `sender.provider` | string |  |
| `sent_at` | date |  |
| `status` | string |  |
| `test_email_body` | string |  |
| `test_email_from` | string |  |
| `test_email_subject` | string |  |
| `total_seeds` | number |  |
| `tracking_code` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /placement-tests/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-placement-test.md) for the provider-specific parameters and requirements.

