# SpamCheck.ai: List Spam Reports

Retrieves saved spam reports from SpamCheck.ai.

```
GET https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpamCheck.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports?${params}`, {
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
| `page` | number | no | Page number of spam reports to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_notes": "string",
      "admin_verified_at": "2026-05-07T12:00:00.000Z",
      "admin_verified_status": "string",
      "body": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "desired_outcome": true,
      "email": "ava@example.com",
      "external_metadata": {},
      "id": 1,
      "ip": "string",
      "notes": "string",
      "result": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin_notes` | string |  |
| `admin_verified_at` | date |  |
| `admin_verified_status` | string |  |
| `body` | object |  |
| `created_at` | date |  |
| `desired_outcome` | boolean |  |
| `email` | string |  |
| `external_metadata` | object |  |
| `id` | number |  |
| `ip` | string |  |
| `notes` | string |  |
| `result` | boolean |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native SpamCheck.ai API, this operation is `GET /spam_reports` (base URL `https://api.spamcheck.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spam-reports.md) for the provider-specific parameters and requirements.

